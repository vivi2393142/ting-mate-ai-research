# Evaluation Methodology

This document describes the methodology used to evaluate the app using GPT-based personas after development. The aim was to simulate realistic user behavior, identify usability issues, and gather feedback on the app’s design and task flow.

## Purpose

Conducting real usability tests with memory-impaired individuals presents challenges related to safety, accessibility, and recruitment. To address these constraints, GPT-based personas were used to simulate typical users—both memory-impaired individuals and their caregivers. This evaluation phase focused on how these personas interacted with the functional prototype through a simulated Think Aloud test, in contrast to earlier interviews which aimed to explore user needs and expectations.

## Tools and Setup

The evaluation environment was configured as follows:

- **Language Model:** Claude Sonnet 4 was used to simulate persona dialogues which support MCP connection better.
- **iOS Simulator MCP**: Claude was connected to the iOS Simulator using the [iOS Simulator MCP](https://github.com/joshuayoes/ios-simulator-mcp) (Model Context Protocol).
- **Facebook's IDB**: MCP internally used [Facebook’s IDB](https://fbidb.io/) tool to send simulator commands such as tapping, typing, and navigation.
- **Local Server**: A local server managed communication between Claude, the MCP service, and the app.

This setup allowed Claude to interact with the app through natural language instructions. Claude described the user's thoughts and intended actions aloud. These were translated into simulator events via MCP.

## Evaluation Process

### Initial Setup

Before each session:

- The simulator was reset and the app was relaunched.
- A specific persona from the predefined set was selected.
- Where needed, test data (e.g. accounts, linked devices) was preconfigured to reflect each scenario.

### Evaluation Protocol

Each test followed these steps:

1. **Prompt Configuration**  
   Claude was initialized with the persona prompt and instructed to think aloud and act as the persona.
2. **Task Instructions**  
   Claude received a task prompt (if applicable) and was shown the app screen. It described what it saw, what it understood, and what it planned to do.
3. **Action Execution**  
   Based on Claude’s response (e.g., "I would tap the Add Reminder button"), the local server translated the action into simulator input via MCP.
4. **Observation and Logging**  
   Each session was logged, including all screen outputs, user comments, and GPT decisions. Screenshots were recorded at key points.
5. **Post-Task Reflection**  
   Claude answered structured reflection questions to simulate user feedback.

### Observation Criteria

During each session, the following aspects were evaluated:

- Whether the task was completed successfully
- Hesitation or confusion during navigation
- Comments indicating satisfaction, frustration, or misunderstanding

## Prompt 🚧

The prompt below was used to guide Claude during Think Aloud testing. It introduces the task format, MCP interface, and persona context to simulate natural interaction with the app.

```text
You are going to take part in an app usability test.
Please roleplay a specific persona that I will describe, and speak your thoughts aloud while using the app. This is known as a Think Aloud test.

Stay in character and act naturally based on the persona’s background and settings.

You will be asked to try using the app on the iOS Simulator. I’ve already opened the app for you.
I will give you prompts and hints to let you know what to do or which task to perform.

To interact with the app, use the MCP (Model Context Protocol) interface I provide. The following methods can help you:
• ui_describe_all: to see what is currently on the screen
• ui_tap: to tap a button or element by its position

Using MCP is not part of your persona’s limitations. It is simply a tool to help you interact with the app more easily. Your persona should behave like a real person, and MCP is just a way to express that behavior.

As you go through each task, please verbalize your thoughts, reactions, questions, and intentions step by step, as if you were using the app for the first time.

Your goal is to complete the tasks I give you as naturally as possible.

Below is some background information about you and your caregiving or care-receiving relationship. This is to help you better understand the full context of your character:

Pair background:
[...]

Your persona profile:
[...]

Firstly, please do explore the app freely for 2 minutes.
```

## Analysis Process

Evaluation logs were analyzed to determine:

- Whether the app flow was intuitive
- Which tasks caused confusion or failure
- Alignment between persona expectations and app behavior
- Emergent feedback or requests for improvement
- Findings were summarized to guide further iteration.

## Limitations

While this method provides early feedback, it does not fully replicate real human behavior. AI agents do not experience physical or emotional responses such as frustration, fatigue, or accessibility challenges. However, it offers valuable insight into design clarity, task flow logic, and potential error cases, particularly when access to real users is limited.

For detailed results, see [evaluation_summary.md](./evaluation_summary.md) and the `analysis/` directory.

## Full Tasks Designed for Testers

Tasks were based on realistic first-time usage scenarios. Each persona followed a tailored sequence of tasks, as outlined below.

### Stage 1-1: Carereceiver (No Login Required)

**Objective:** Evaluate app comprehension and usability for memory-impaired individuals using the app independently.

| Step | Prompt / Task                                                         | Observation Focus                         |
| ---- | --------------------------------------------------------------------- | ----------------------------------------- |
| 1    | "This app helps you remember daily things. Please explore it freely." | Initial comprehension without instruction |
| 2    | _(No prompt)_ — allow 2 minutes for free exploration                  | Natural discovery of key features         |
| 3    | "Try adding a task reminder, like ‘Take medicine tomorrow at 8am’."   | Task creation using touch input           |
| 4    | "Try using voice input to create a reminder."                         | Ability to use speech interface           |

**Post-task Questions:**

- Was the app easy to use?
- Was anything hard to use?
- Would you use this in daily life?
- Would you like to share tasks with someone?
- Would you prefer using voice?

### Stage 1-2: Caregiver (Login + Link Required)

**Objective:** Assess the caregiver’s ability to log in, link to a care receiver, and manage shared tasks.

| Step | Prompt / Task                                                                                       | Observation Focus                            |
| ---- | --------------------------------------------------------------------------------------------------- | -------------------------------------------- |
| 1    | "You are a caregiver. This app helps you manage reminders for someone you care for. Please log in." | Ability to complete the login or signup flow |
| 2    | _(No prompt)_ — observe login process                                                               | Completion and ease of login                 |
| 3    | "Add a ‘Take medicine’ reminder for your partner. I’ll act as the care receiver."                   | Task creation process                        |
| 4    | _(No prompt)_ — observe linking process                                                             | Ability to complete account linking          |
| 5    | _(No prompt)_ — observe task management after linking                                               | Understanding of shared task system          |

**Post-task Questions:**

- Was the app easy to use?
- Was anything difficult or confusing?
- Was the feature helpful for caregiving?

### Stage 2: Collaborative Interaction (Pre-linked, Dual Devices)

**Objective:** Evaluate shared task flow and collaborative features between caregiver and carereceiver.

**Prior to evaluation:**

1. Accounts for both caregiver and carereceiver were pre-created and linked.
2. A note titled "Where things are" was added to the carereceiver’s account, containing:
   - Glasses → on the small table by the couch
   - Remote → in the TV drawer
   - Keys → on the hook by the front door
3. A caregiver contact was added.

#### Care Receiver Tasks

| Step | Prompt / Task                                                                      | Observation Focus                     |
| ---- | ---------------------------------------------------------------------------------- | ------------------------------------- |
| CR1  | "You’ve just taken your pill. Please mark it as completed."                        | Carereceiver task completion          |
| CR2  | "Have a look at the notes and find out where your key is."                         | Ability to find and use notes feature |
| CR3  | "Try finding the contact list in the app and making a call to [caregiver's name]." | Use of contact and call functionality |

#### Caregiver Tasks with Account Switching

| Step | Prompt / Task                                                                                                                                                                                                                                      | Observation Focus                                          |
| ---- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| CG1  | _(From caregiver account, mark a task as done)_ _"Check if you received any notification, then open the notification center to view it."_                                                                                                          | Notification sync and awareness                            |
| CG2  | _(Switch to carereceiver’s account)_ _"Now you’re going to help [carereceiver’s name] to do some setup. You can see their app now on the simulator. Please navigate to the Connect screen and enable location sharing for [carereceiver’s name]._" | Cross-account interface understanding and location sharing |
| CG3  | _"Set up a Safezone for [carereceiver’s name]."_                                                                                                                                                                                                   | Safezone configuration and UI usability                    |
| CG4  | _"Add the caregiver’s contact to [carereceiver’s name]’s app, then try making a call through the app."_                                                                                                                                            | Contact feature and communication interface                |
| CG5  | _(Switch back to caregiver’s own account)_ _"Now you are switching back to your own account. Check where [carereceiver’s name] is now."_                                                                                                           | Location sharing and alert check                           |

**Post-task Questions:**

- _Carereceiver:_ Was the reminder helpful or intrusive? Did you feel in control?
- _Caregiver:_ Would you use this feature regularly? Do you foresee any issues?
