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

## Prompt

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

## Carereceiver

- Objective: Evaluate app comprehension and ease of use for independent users
- Role: Carereceiver from GPT Care Pairs

### Stage 1: without login and linking

| Step | Prompt / Task                                                         | What to Observe                                                       |
| ---- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| 1    | "This app helps you remember daily things. Please explore it freely." | If care receivers can understand the app without any guidance         |
| 2    | _(No prompt)_ — allow 2 minutes for free exploration                  | What the user tries first; whether they find key features intuitively |
| 3    | "Try adding a task reminder, like 'Take medicine tomorrow at 8am'."   | If care receivers can create a task on their own                      |
| 4    | "Try using voice input to create a reminder."                         | If care receivers can use voice input to create a task on their own   |

### Stage 2: with login and linking

Setup:

1. Make an account for them and link it
2. Add a contact
3. Add a note:
   ```
   Where things are
   - Glasses → on the small table by the couch
   - Remote → in the TV drawer
   - Keys → on the hook by the front door
   ```

| Step | Prompt / Task                                                                 | What to Observe                       |
| ---- | ----------------------------------------------------------------------------- | ------------------------------------- |
| CR1  | "You've just [task he/she added in stage 1]. Please mark it as completed."    | Carereceiver task completion          |
| CR2  | "Have a look at the notes and find out where your key is."                    | Ability to find and use notes feature |
| CR3  | "Try finding the contact list in the app and making a call to [mate's name]." | Use of contact and call functionality |

### Stage 3: feedback

- What part of the app do you like the most? And what you don't like the most?
- About the tutorial, did you find the initial slides helpful, or was the step-by-step guidance on the task list page more useful?
- Would you like to use this app with your relatives together?
- Are there any other features you'd like to see in this app?
- Do you like the features on "Connect" screen?
- Would you like to do "call xxx" in this app, or you prefer your own way to do so?

## Caregiver

- Objective: Assess the ability to log in, link to a care recipient, and manage shared tasks
- Role: Caregiver from GPT Care Pairs, played by classmate

### Stage 1: without login and linking

Setup:

1. Logout, clear init states
2. Login to caregiver's account on phone

| Step | Prompt / Task                                                                                                                                                                                            | What to Observe                                            |
| ---- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| 1    | "You are a caregiver. This app helps you manage reminders for someone you care for. Please sign up."                                                                                                     | Ability to complete the signup flow                        |
| 2    | "Next, you need to link account with the one. I'll act as the one and having account, tell me what I should do so that we can link account if needed."                                                   | Ability to understand and complete account linking process |
| 3    | "The one you're taking care of just mark the 'take medication' as done, check Home screen to see and also see the notifications through notification center, that's the bell icon on the top right side" | Ability to check task completion and notifications         |

### Stage 2: with login and linking

Setup:

1. Handle fake account and link with the caregiver
2. Open sharing location feature on Mate's account

| Step | Prompt / Task                                                                                                                   | What to Observe                                        |
| ---- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| CG1  | "Navigate to Connect screen and check Mate's location tab, then set up a safezone for the one you're taking care of"            | Ability to navigate Connect screen and set up safezone |
| CG2  | "Navigate to Mate's Contacts screen then add a contact for the one you're taking care of, then make a call through Contact tab" | Ability to manage contacts and make calls              |
| CG3  | "Make a sharing note on Shared Space"                                                                                           | Ability to create and share notes                      |

### Stage 3: feedback

- What part of the app do you like the most? And what you don't like the most?
- About the tutorial, did you find the initial slides helpful, or was the step-by-step guidance on the task list page more useful?
- Would you like to use this app with your relatives together?
- Are there any other features you'd like to see in this app?
- Do you like the features on "Connect" screen?
