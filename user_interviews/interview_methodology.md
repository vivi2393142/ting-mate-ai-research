# Interview Methodology

This document outlines the methodology used to simulate user interviews through GPT-based personas during the early stages of app design. The goal was to gather realistic insights into the needs, behaviors, and expectations of memory-impaired individuals and their caregivers.

## Purpose

Conducting real interviews with memory-impaired individuals presents difficulties such as recruitment constraints, ethical concerns, and communication barriers. To mitigate these challenges, simulated interviews were conducted using large language models. These interviews provided early insights into user needs and supported iterative design decisions when direct access to target users was limited.

## Tools and Setup

- **Language Model:** ChatGPT (GPT-4) was used to simulate persona dialogues.
- **Prompt Design:** Each interview began with a carefully structured persona prompt, containing:

  - Background: age, memory condition, tech familiarity, living situation
  - Daily routines, emotional tone, and caregiving context

- **Questionnaires:** Two sets of questionnaires were created: one for care receivers and one for caregivers.
- **Interaction Style:** A multi-turn think-aloud style was used, where GPT responded as if it were the persona being interviewed.
- **Review Process:** Responses were manually reviewed to ensure alignment with persona traits and to identify insights relevant to app design.

## Interview Process

1. **Persona Initialization**
   - Select one of the eight predefined personas.
   - Load the full background and constraints into the GPT system prompt.
2. **Interview Execution**
   - Use one of the two questionnaire sets.
   - Proceed through each question one by one in natural dialogue form.
   - Allow the persona to elaborate where appropriate.
3. **Answer Logging**
   - Save all responses in markdown format.
   - Each persona session was saved as a separate file for later analysis.
4. **Result Verification**
   - Check for consistency between answers and persona profiles.
   - Note moments of hesitation, contradiction, or particularly insightful comments.
5. **Insight Extraction**
   - After completing interviews, responses were coded and categorized.
   - Recurring themes, needs, frustrations, and feature suggestions were summarized.

## Analysis Process

Interview transcripts were analyzed manually to identify:

- Common needs shared across personas
- Pain points in memory management or caregiving
- Preferred modes of interaction (voice vs. touch)
- App features viewed as essential or confusing

Insights from this analysis were summarized in structured tables and used to inform:

- Initial wireframes and UI design
- Feature prioritization
- Task scenarios for prototype evaluation

For complete transcripts and extracted insights, see the `user_interviews/` folder and `interview_summary.md`.

## Full Interview Questionnaires

### Question Set for Memory-Impaired Individuals

1. Current Behavior

   - Can you describe what a normal day looks like for you?
   - Does anyone help you with your daily routine? If so, how do they assist you?
   - Do you use anything to help you remember things, like notes, alarms, or reminders from people?
   - What things do you forget most often?

2. Challenges

   - Are there times when forgetting something causes problems or stress for you?
   - Do you sometimes feel confused or unsure about what's happening during the day?
   - When you forget something, how do you usually handle it?

3. Tech Familiarity & UI Attitudes

   - Do you use a smartphone or tablet? What do you use it for?
   - Have you ever used any apps to remind you of things?
   - When using apps, what makes them easy or difficult for you?
   - When texting or using apps, do you prefer voice control or touch control?

4. Needs

   - What kind of help would you want from your daily life?
   - What kind of help would you _not_ want?
   - Are there tasks you prefer to do on your own? What tasks would you rather someone help you with?
   - Would it be helpful to have gentle reminders for important things, like meals or medicine?

5. App Introduction & Feedback

   Participants were given the following explanation:

   > _"We're designing a simple app that helps people remember daily routines or important things like meals, medicine, or appointments. It can also help them feel more confident throughout the day."_

   Then asked:

   - What do you think about this kind of app?
   - Would you like to try using something like this?
   - What would you want this app to do for you?
   - What worries or questions would you have about using it?
   - What tasks will you set on the app?

### Question Set for Caregivers

1. Current Behavior

   - Can you describe your daily caregiving routine?
   - How do you help the person you care for remember things, like medicine or appointments?
   - Are other family members involved in caregiving? If so, how do you coordinate?

2. Challenges

   - What are the most difficult parts of your caregiving role?
   - Are there times when you feel anxious about their safety or well-being?
   - How do memory problems affect your own schedule or energy?

3. Tech Familiarity & UI Attitudes

   - Do you or your family member use phones or apps for health or reminders?
   - What types of tech have you tried (if any) to assist with care?
   - What makes a digital tool easy or hard for you and them to use?

4. Needs

   - In what areas do you wish you had more support as a caregiver?
   - Would it help if you could check in on their routine remotely?
   - What kind of features would make a memory-support app truly helpful for your situation?

5. App Introduction & Feedback

   Participants were given the following explanation:

   > _"We're building an app designed to support both people with memory difficulties and their caregivers. It offers reminders, daily structure, and remote check-ins to reduce stress."_

   Then asked:

   - What features would be most useful to you personally?
   - How do you feel about this kind of app?
   - Is there anything you'd be worried about using or setting up?
   - Would you be willing to try it with the person you care for?
   - What tasks will you set on the app?
