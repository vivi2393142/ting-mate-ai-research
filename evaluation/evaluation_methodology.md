# Evaluation Methodology

This document explains how GPT-based personas were used to evaluate the app after development. The purpose was to simulate real user behavior, identify usability issues, and collect feedback on app design and task flow.

## Purpose

Real usability testing with memory-impaired individuals is difficult due to accessibility, safety, and recruitment barriers. To work around this, GPT personas were used to perform simulated evaluations. Unlike earlier interviews, this phase focused on how new users interact with the working prototype.

## Tools and Setup

To simulate realistic app usage:

- The evaluation was conducted using **Claude Sonnet 4** as the AI agent.
- Claude was connected to the iOS Simulator via the [iOS Simulator MCP](https://github.com/joshuayoes/ios-simulator-mcp) (Model Context Protocol).
- MCP internally uses [Facebook’s IDB](https://fbidb.io/) tool, which allows code to control the iOS Simulator by sending commands like tapping, typing, or launching apps.
- A local server handled communication between Claude, the MCP, and the running app.

This setup allowed Claude to “use” the app by describing actions in natural language. Claude responded to each screen, and MCP triggered corresponding updates in the simulator.

## Persona Configuration

The same GPT persona structure was used as in interviews, but each evaluation run started fresh — without memory of prior conversations. This helped simulate a first-time user experience.

Each persona included:

- Memory-impaired individuals or caregivers
- A structured background (age, habits, tech comfort, etc.)
- Behavior goals and typical support needs

See [personas/](../) for detailed persona definitions.

## Evaluation Process

1. **Prompt Setup**
   Claude was given the same structured persona prompt format used during interviews. It was instructed to think aloud and behave as the assigned user.

2. **Think-Aloud Simulation**
   Each evaluation used a _think-aloud_ method. Claude would describe what the user sees, what they are thinking, and what they would do next.

3. **Screen-by-Screen Flow**
   The app UI was shown one screen at a time. Based on Claude’s response (e.g. “I would tap ‘Add Reminder’”), the next screen was triggered via MCP.

4. **Logging & Review**
   The full dialogue was recorded for each task. The log included screenshots and persona actions for later analysis.

See [process_design.md](./process_design.md) for task design and screen sequencing.

## Tasks

Each persona was given common tasks like:

- Check today’s tasks
- Add a reminder using voice
- Find shared notes

These were selected to reflect realistic first-use experiences.

## Differences from Interviews

- Interviews were about _understanding needs_; evaluations tested _actual interaction_.
- Interviews used ChatGPT; evaluations used Claude for better local and MCP compatibility.
- Evaluations started with a clean persona context (as if a new user encountering the app for the first time).

## Limitations

This method does not fully replicate human testing. AI agents lack true frustration, confusion, or accessibility needs. However, it provides early insight into design clarity, navigation logic, and error cases — especially when access to users is limited.

See [evaluation_summary.md](./evaluation_summary.md) and `analysis/` for findings and persona-specific evaluations.
