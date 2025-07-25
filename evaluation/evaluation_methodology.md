# Evaluation Methodology

This document describes the methodology used to evaluate the app using GPT-based personas after development. The aim was to simulate realistic user behavior, identify usability issues, and gather feedback on the app’s design and task flow.

## Purpose

Conducting real usability tests with memory-impaired individuals presents challenges, including safety, accessibility, and recruitment limitations. To address this, GPT-based personas were employed to simulate the behavior of typical users, including both memory-impaired individuals and their caregivers. This evaluation phase focused on how these personas interacted with the functional prototype, in contrast to earlier interviews which were used to explore needs and expectations.

## Tools and Setup

The evaluation environment was configured as follows:

- The AI agent was **Claude Sonnet 4**.
- Claude was connected to the iOS Simulator using the [iOS Simulator MCP](https://github.com/joshuayoes/ios-simulator-mcp) (Model Context Protocol).
- MCP internally used [Facebook’s IDB](https://fbidb.io/) tool to send simulator commands such as tapping, typing, and navigation.
- A local server managed communication between Claude, the MCP service, and the app.

This setup allowed Claude to interact with the app through natural language instructions. Claude described the user's thoughts and intended actions aloud. These were translated into simulator events via MCP.

## Persona Configuration

The same structured personas used during the interview phase were reused here. Each evaluation session began with a new prompt, without memory of previous interactions. This approach simulated a true first-time user experience.

Each persona included:

- Background: age, habits, digital literacy, relationship status
- Goals: memory support needs or caregiving responsibilities
- Behavior: likely usage patterns, preferences (e.g. voice interaction)

See the [personas_design](process_design.md) for detailed definitions of each GPT persona pair.

## Evaluation Process

### Initial Setup

Before each session:

- The simulator was reset and the app was relaunched.
- Claude sessions were started fresh to prevent memory leakage.
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

4. **Screen Progression**  
   The app advanced to the next screen or state based on the user action.

5. **Observation and Logging**  
   Each session was logged, including all screen outputs, user comments, and GPT decisions. Screenshots were recorded at key points.

6. **Post-Task Reflection**  
   Claude answered structured reflection questions to simulate user feedback.

### Observation Criteria

During each session, the following aspects were evaluated:

- Whether the task was completed successfully
- Hesitation or confusion during navigation
- Comments indicating satisfaction, frustration, or misunderstanding

## Task Design

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

#### Prior to evaluation:

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

## Differences from Interviews

| Aspect | Interviews                     | Evaluations                          |
| ------ | ------------------------------ | ------------------------------------ |
| Focus  | Understanding needs            | Testing actual interactions          |
| Tool   | ChatGPT                        | Claude Sonnet 4                      |
| Memory | Ongoing session memory         | Clean, stateless runs                |
| Output | Requirements and feature ideas | Usability insights and behavior logs |

## Limitations

While this method provides early feedback, it does not fully replicate real human behavior. AI agents do not experience physical or emotional responses such as frustration, fatigue, or accessibility challenges. However, it offers valuable insight into design clarity, task flow logic, and potential error cases, particularly when access to real users is limited.

For detailed results, see [evaluation_summary.md](./evaluation_summary.md) and the `analysis/` directory.
