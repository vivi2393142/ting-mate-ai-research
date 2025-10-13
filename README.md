# Ting Mate – AI-Assisted User Research and Evaluation

This repository explains the **AI-assisted research stages** of [Ting Mate](https://github.com/vivi2393142/ting-mate-frontend), a mobile app designed for memory-impaired individuals and older adults.

It focuses on two key phases: **User Research** and **Evaluation**, both powered by Large Language Models (LLMs).

```mermaid
graph LR
  A[Literature Review<br/>& Problem Definition] --> B["AI-Assisted</br>User Research"]
  B --> C["FE & BE</br>Development"]
  C --> D["AI-Assisted</br>Evaluation"]
  D --> E["Findings &</br>Refinement"]

  style B stroke-width:5px
  style D stroke-width:5px
```

In these stages, simulated personas were used to gather user needs and test usability when real participants were difficult to reach. The insights guided the app’s design, accessibility features, and task workflows.

## AI-Assisted User Research

```mermaid
graph LR
    subgraph A[Preparation]
        A1[Set</br>researchgoals]
        A2[Design personas</br>& background]
        A3[Prepare</br>interview questions]
        A1 --> A2 --> A3
    end

    subgraph B[Simulation in ChatGPT]
        B1[Load persona</br>into ChatGPT]
        B2[Conduct</br>interviews]
        B3[Record</br>responses]
        A3 --> B1 --> B2 --> B3
    end

    subgraph C[Analysis]
        C1[Code</br>key ideas]
        C2[Identify needs</br>& insights]
        B3 --> C1 --> C2
    end
```

GPT-based personas were created with demographic and contextual backgrounds. Then, they engaged in multi-turn interviews to express needs, frustrations, and expectations. Lastly, responses were coded to identify design priorities, accessibility challenges, and recurring themes.

## AI-Assisted Evaluation

```mermaid
sequenceDiagram
  participant Dev as Evaluator
  participant LLM as Claude Sonnet 4
  participant Sim as iOS Simulator
  Dev->>LLM: Send persona background prompt
  loop For each task instruction<br>with ongoing think-aloud
    Dev->>LLM: Provide task instruction
    LLM->>Sim: Call ui_describe_all (via MCP)
    Sim-->>LLM: Return screen information
    LLM->>Sim: Send ui_tap / ui_type / ui_swipe (via MCP)
    Sim-->>LLM: Call ui_describe_all again
  end
```

LLM personas operated the Ting Mate app through the iOS Simulator using the Model Context Protocol (MCP). They received screen descriptions, performed actions (tap, type, swipe), and provided real-time think-aloud feedback. This enabled automated usability testing and refinement without human participants.

## Repository Structure

| Folder                                       | Description                                                |
| -------------------------------------------- | ---------------------------------------------------------- |
| [`personas_design.md`](./personas_design.md) | Persona definitions and creation methods                   |
| [`user_research/`](./user_research/)         | Interview stage: prompts, transcripts, analysis            |
| [`evaluation/`](./evaluation/)               | Evaluation stage: methodology, transcripts, coded findings |

## Related Repositories

- [Ting Mate – Frontend (React Native + Expo)](https://github.com/vivi2393142/ting-mate-frontend)
- [Ting Mate – Backend (FastAPI)](https://github.com/vivi2393142/ting-mate-backend)
