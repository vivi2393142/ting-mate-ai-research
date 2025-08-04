# Participant Profile

- **Date**: 2025-08-04
- **Participant**: Jacky
- **Role**: Care Receiver
- **Test Platform**: iOS Simulator via MCP (Claude Desktop)
- **Simulated Account**: [Jacky@gmail.com](mailto:Jacky@gmail.com)

## Background

See Jacky in Set 4 – [Persona Profiles](personas_design.md)

## Execution Summary

### Stage 1: without login and linking

| #   | **Planned Prompt / Task**                                               | Execution              | Completed | Notes                                                               |
| --- | ----------------------------------------------------------------------- | ---------------------- | --------- | ------------------------------------------------------------------- |
| 1   | _"This app helps you remember daily things. Please explore it freely."_ | (No prompt)            | Yes       | Completed naturally without any hint.                               |
| 2   | _(No prompt)_ — allow 2 minutes for free exploration                    | (No prompt)            | Yes       | Explored all main features independently.                           |
| 3   | _"Try adding a task reminder, like ‘Take medicine tomorrow at 8am’."_   | (No prompt)            | Yes       | Created reminder manually, but had difficulty setting correct time. |
| 4   | _"Try using voice input to create a reminder."_                         | Simulated via GPT text | Yes       | Created “walk my dog at 6 PM” task with perfect recognition.        |

### Stage 2: with login and linking

| #   | **Planned Prompt / Task**                                           | Execution                | Completed | Description                                        |
| --- | ------------------------------------------------------------------- | ------------------------ | --------- | -------------------------------------------------- |
| 5   | _"You’ve just taken your pill. Please mark the task as completed."_ | Tried during Stage 1     | No        | Could not locate checkbox; attempted edit instead. |
| 6   | _"Have a look at the notes and find out where your key is."_        | No further prompt        | Yes       | Found shared note in “Connect” page.               |
| 7   | _"Try finding the contact list and making a call."_                 | Skipped (no mate linked) | —         | Not applicable in this test case.                  |

## Findings

### Strengths

| Category              | Summary                   | Description                                                      | Supporting Quote                                                                 |
| --------------------- | ------------------------- | ---------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| Voice Input           | Fast and intuitive        | Created task accurately with natural speech.                     | _“The voice feature alone could be life-changing for daily routine management.”_ |
| Shared Notes          | Reinforced independence   | Notes about item locations reduced daily stress.                 | _“This is incredibly helpful... this is invaluable.”_                            |
| Task Management       | Easy to understand        | Successfully created/edit tasks and understood recurrence rules. | _“This is exactly what I need to help manage my daily routine.”_                 |
| Onboarding Guidance   | Step-by-step flow helped  | Contextual tutorial was effective without being overwhelming.    | _“What made the tutorial good was that it didn’t overwhelm me.”_                 |
| Notification Settings | Offered control           | Enabled overdue/task reminders; user appreciated flexibility.    | _“Both of these would be really helpful for me.”_                                |
| Emotional Tone        | Empowering and respectful | Felt supported, not monitored.                                   | _“This app really feels designed with people like me in mind...”_                |

### Areas for Improvement

| Category            | Short Summary           | Description                                            | Supporting Quote                                                                     |
| ------------------- | ----------------------- | ------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| Time Picker         | Difficult to use        | Slider UI made time setting imprecise and frustrating. | _“Those tiny sliders are really difficult to use precisely.”_                        |
| Tutorial Redundancy | Unexpected retriggering | Settings tutorial appeared again, causing confusion.   | _“I got a bit confused... another tutorial sequence.”_                               |
| Location Sharing    | Felt intrusive          | Concerned about being tracked prematurely.             | _“I don’t want to feel like I’m being tracked... it assumes I’m less capable.”_      |
| Shared Logs         | Privacy unclear         | Concerned about surveillance and lack of control.      | _“If it’s logging my every movement... that would feel too much like surveillance.”_ |

## Evaluation Insights

Jacky, a 50-year-old living with younger-onset Alzheimer’s, explored Ting Mate confidently and found value in the app’s focus on voice input, shared notes, and routine tracking. His feedback emphasized the importance of dignity and user control over shared data. While he praised features that helped with independence, he flagged several UX issues around precision input and onboarding clarity. He expressed strong interest in using the app regularly, if privacy and simplicity are respected.

### **Recommendations**

- Replace slider-based time picker with clearer alternatives (e.g., presets, number input).
- Avoid triggering duplicate tutorials in Settings.
- Improve visual orientation during navigation (breadcrumbs or clearer hierarchy).
- Continue enhancing voice command accuracy and confirmations.

**Suggested Feature Additions:**

- Attach photos to reminders or notes (visual reinforcement)
- Emergency shortcut button (contact trusted caregiver)
- Medication tracking with dosage and check-off confirmation
- Routine templates (e.g., “morning routine,” “evening prep”)
- Voice note recording for thoughts or memory aids
- Simple calendar view combining tasks and events
- Controlled sharing: Let users decide what to share, when, and with whom
- Smoother transitions between app sections (clarity in navigation)

## Test Method Notes

Test was conducted using Claude roleplaying as Jacky in a think-aloud protocol. Interaction was simulated through Model Context Protocol (MCP) via iOS Simulator. Some features (e.g., checkbox tap, call actions) were not operable due to simulation limitations.

## Full Transcripts

### Stage 1: First-time use without login or account setup

<details>
<summary>Q1</summary>

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

(Persona background omitted here; see [Background](#background) section above.)

Your persona profile:

(Persona background omitted here; see [Background](#background) section above.)

Firstly, please do explore the app freely for 2 minutes

</details>

<details>
<summary>A1</summary>

I'm Jacky, a 50-year-old social worker living with younger-onset Alzheimer's. I'm generally optimistic and tech-savvy, though I sometimes have memory lapses. Let me start by seeing what's on this app screen.\*_Oh, this looks like a welcome screen for an app called "Ting Mate." I can see it's showing me some onboarding information. The main message says "Stay on Top of Your Day" and mentions creating simple reminders and checking off tasks like medicine or appointments. That actually sounds really helpful for someone like me - I could use help staying organized with my daily routine and medications._

I can see there are some dots at the top that suggest this might be a slideshow introduction, and there's a "Next slide" button. Let me tap that to see what else this app can do.**Good, that worked. Let me see what's on the next screen.**Ah, this is interesting! Now it's showing "Use It Together" and explaining that I can share tasks with a "mate" I trust, or connect to manage someone else's shared tasks. This could be really useful for me - I have family members who help me when I'm having more difficult days. Being able to share my tasks with them would give me extra support and accountability.\*

The dots show I'm on the second screen now. Let me continue to see what else this app offers.\*_Now this screen says "Stay Close, Even from Afar" and mentions getting alerts when your mate leaves a safe zone. Hmm, this sounds more like location tracking. I'm not sure how I feel about that - I value my independence and don't necessarily want to be tracked all the time. Though I understand this could be helpful for some people with memory issues who might get lost. For me personally, I'm still living independently and getting around fine on my own._

Let me continue to see what else this app offers. Maybe there are features that would be more relevant to my situation.\*_Perfect! Now I'm at what looks like a main setup screen asking "How do you plan to use Ting Mate?" I can see two main options:_

_1. "Try It for Yourself" - This sounds like it would be for me to use independently2. "Connect with Mates" - This would be for sharing with family or friends_

_As someone living independently with younger-onset Alzheimer's, I think I'd like to start by trying it for myself first. I want to see what the app can do for me personally before deciding whether to involve my family members. I like to maintain my independence when possible._

Let me tap on "Try It for Yourself" to see what that leads to.\*_Great! It looks like I'm now in the main app interface and there's some kind of tutorial happening. I can see a "1" in the top left corner, suggesting this is step 1 of a tutorial. The main area says "Tasks will show up here" - so this must be where I'll see my reminders and to-do items once I create them._

There are "Skip" and "Next" buttons at the bottom. Since I'm exploring and want to understand how to use this app properly, let me tap "Next" to continue with the tutorial. I find it helpful to go through instructions step by step, especially when learning new technology.\*_Now I'm on step 2 of the tutorial. It's showing me "Tap here to add a task." This is helpful - it's teaching me how to add reminders or tasks. I can see there are now three buttons: "Skip", "Previous", and "Next". This is good interface design - I can go back if I missed something or skip ahead if I want to._

Since this is showing me how to add tasks, which is exactly what I need for managing my medications and appointments, let me continue with the tutorial to learn the proper way to do this.\*_Excellent! Now I'm on step 3, the final step of the tutorial. It's telling me "You can also edit tasks with your voice." This is actually really appealing to me - voice input could be especially helpful on days when I'm having more difficulty with memory or fine motor skills. Being able to just speak my reminders instead of having to type them out could make this app much more accessible for me._

I can see there are "Previous" and "Finish" buttons. Since this appears to be the end of the tutorial, let me tap "Finish" to complete it and start using the app.\*_Perfect! Now I'm in the main app interface. I can see "Today's Tasks" at the top, and it's telling me "You haven't added any tasks yet" and "Add a task to get started!" This is exactly what I expected._

_I can see several key elements:1. A big "Add Task" button in the middle - this is what I need to start creating my reminders2. A large circular "Start Voice Command" button at the bottom - this is that voice feature they mentioned3. A notifications button in the top right4. Bottom navigation with "Connect", a middle button (unlabeled), and "Settings"_

As someone who needs help managing my daily routine and medications, let me try adding my first task. I'll start with something simple but important - my morning medication reminder. Let me tap the "Add Task" button.\*_Excellent! I'm now in the "Add Task" screen. I can see several fields to fill out:_

_1. **Title** - with a text field that says "Add task title"2. **Icon** - shows a green checkmark with up/down arrows_

_3. **Time** - currently set to "16:00" with up/down arrows4. **Repeat** - set to "Daily" with up/down arrows_

This is perfect for setting up my medication reminder! Let me start by adding a title for my morning medication. I'll tap on the title field and enter something like "Take morning medication".**Now I need to clear the placeholder text and type my own title. Let me type my medication reminder.**Good! Now I need to set the time. The current time shows 16:00 (4 PM), but I want this for my morning routine. I usually take my medication around 8 AM, so let me change that time. I'll tap on the time field.\*_Perfect! The time picker has opened up and I can see two sliders - one for hours and one for minutes. The current values show 5007 and 4980 respectively, which seems to correspond to 16:00 (4 PM). I need to change this to 08:00 for my morning medication._

I need to adjust the hour slider first to get to 8 AM. Let me try sliding the first slider (hours) to change it from 16 to 08.**I see the time has changed to 14:00 (2 PM), so the slider is working. I need to continue adjusting it to get to 08:00. Let me try tapping the time field again to open the time picker and make a more precise adjustment.**The time picker is open again. I need to drag the hour slider (the first one) down to reduce the hour from 14 to 08. Let me try a swipe gesture to move it down more significantly.**Great! The time is now showing 06:00 (6 AM), which is close to what I want. I need to adjust it to 08:00 (8 AM), so I need to move it up just a little bit. Let me tap on the time again to adjust it slightly.**The time is still showing 06:00. Let me try another small adjustment upward to get it to 08:00.**Let me tap outside the time picker to close it and see what time I have set, then continue with creating the task.**Now it shows 04:00 (4 AM), which is too early for my morning medication. You know what, let me just work with a reasonable time for now. 4 AM isn't ideal, but I can always edit this later. The important thing is to get familiar with how this app works.\*

_I can see the other settings look good:- **Title**: "Take morning medication" ✓- **Icon**: Green checkmark (seems appropriate) ✓- **Time**: 04:00 (I'll adjust this later if needed)- **Repeat**: Daily (perfect for medication) ✓_

I notice there should be a "Save" or "Done" button somewhere to complete creating this task. Let me scroll down or look for navigation buttons.**I notice there's a nav bar at the top that says "Add Task" but I don't see any obvious save button. Maybe there's a save button in the navigation bar or maybe I need to look at the top navigation. Sometimes apps have a "Done" or "Save" button in the top right. Let me check what's available by tapping in the navigation area.**Perfect! There's a "Done" button in the top right corner. This makes sense - that's exactly what I need to save my task. Let me tap on it to complete creating my morning medication reminder.\*_Excellent! My task has been created successfully! I can see it's now showing in my "Today's Tasks" list:_

_"✅ Take morning medication Daily 04:00 checkbox"_

_This is really encouraging! Even though the time is set to 04:00 instead of my preferred 08:00, I've successfully created my first task. I can see:- The green checkmark icon- The title "Take morning medication"_

_"Daily" repetitionA checkbox to mark it as completed_

_This is exactly what I need to help manage my daily routine. Having visual reminders for my medication will be very helpful, especially on days when my memory isn't as sharp. The fact that it repeats daily means I won't have to recreate it every day._

_I notice the "Add Task" button is still there, so I could easily add more reminders for other important things like appointments, exercise, or taking my dog for walks. And there's still that large voice command button at the bottom that I'm curious about._

Let me try that voice feature they mentioned in the tutorial - it could be really useful for quickly adding tasks when I'm busy or having difficulty typing.\*_Fantastic! The voice command interface has opened up and it's showing me example commands I can use. This is really helpful! I can see:_

_"Try asking me..."- "Remind me to take my pills at 2 every day"- "Change my pill reminder to 4 p.m."_

- _"Can you delete the 'take medicine' task?"_

_It says "I'm listening" at the bottom, and the button has changed to "Stop Voice Command". This is perfect! These examples are very relevant to my situation. The second example is particularly useful - "Change my pill reminder to 4 p.m." could help me fix the timing on the task I just created._

Since this is a simulation and I can't actually speak, let me close this voice interface for now and continue exploring. I love that this feature exists though - being able to just speak commands like "remind me to walk the dog at 6 PM" would be so much more convenient than typing everything out, especially when I'm having a difficult day.**Good, I'm back to the main screen with my task showing. Let me try exploring the other parts of the app. I notice there's a "Settings" button in the bottom navigation. As someone who likes to understand how technology works and customize it for my needs, let me check what settings are available.**Interesting! It seems like I've triggered another tutorial or setup process. I can see this is step 1 of something, and it's talking about "Bigger text and simple design for easier reading." This actually sounds very appealing to me! As someone living with Alzheimer's, having larger text and a simpler interface would be really helpful, especially on days when I might be having more difficulty with visual processing or concentration.\*

This is a thoughtful accessibility feature. Let me continue with this setup to see what options are available.\*_Now I'm on step 2, and it's explaining "Connect with your mates here to share and stay in sync." This is referring to that sharing feature I saw in the onboarding. While I like to maintain my independence, I can see how this could be valuable for connecting with family members who help support me. They could see my medication reminders and help ensure I'm staying on track with my routine._

Let me continue to see what other setup options there are.\*_This is step 3, the final step, and it's asking about logging in to "connect a mate and use all features." I see there are "Previous" and "Finish" buttons. Since I'm still just exploring the app and getting comfortable with it myself, I think I'll finish this setup for now. I can always come back and set up the mate connection later if I decide that would be helpful._

For now, I'm more focused on learning how to use the basic task management features for my own daily routine.\*_Perfect! Now I'm in the actual Settings screen and can see all the customization options available. This is really comprehensive and well-organized! Let me look at what's available:_

**GENERAL:\***- Text Size: Currently set to "Standard" - I could change this to larger text which would be helpful- Display Mode: Set to "Full" - I'm not sure what this means but I like that there are options\*

**NOTIFICATION:\***- Notification: Currently "Off" - I should probably turn this on so I get alerts for my medication\*

**CONNECT:\***- Information about connecting with mates- Allow Location Sharing: There's a toggle switch that appears to be off\*

**ACCOUNT:\***- Name and Login/Sign Up options\*

The notification setting catches my attention - having notifications for my medication reminders would be really important. Let me turn that on.\*_Excellent! I'm now in the notification settings and can see the specific options:_

_1. **Task Reminder**: "Notify when it's time to do a task" - This toggle appears to be off2. **Overdue Reminder**: "Notify again if a task is not done on time" - This toggle also appears to be off_

Both of these would be really helpful for me! The task reminder will alert me when it's time to take my medication, and the overdue reminder is particularly valuable since I sometimes forget or get distracted. Let me turn both of these on.**Now let me turn on the overdue reminder as well.**Great! Now I should have both notification types enabled. Let me go back to see the main settings and maybe return to my tasks. I'll look for a back button or try to navigate back.**I see there's a "Cancel" button in the top left. Let me tap that to go back.**Good, I'm back in the main settings screen. I notice the notifications still show "Off" in the main view, but I did enable those specific notification types. Now let me go back to the Home screen to see my tasks and maybe try creating another task. I'll tap the "Home" button in the bottom navigation.**Perfect! I'm back on the home screen and I can see my medication task is still there: "✅ Take morning medication Daily 04:00 checkbox". Now let me try one more thing - I want to see what happens when I tap on the existing task. Maybe I can edit it or mark it as completed.**Excellent! I'm now in the "Edit Task" screen for my medication reminder. I can see all the same fields as when I created it:\*

**\*Title**: "Take morning medication"**Icon**: Green checkmark**Time**: "04:00" (still showing the early time)**Repeat**: "Daily"\*

_And I notice there's a new option at the bottom: "trash Delete Task" - this would let me remove the task if I needed to._

This is perfect! Now I can fix the time from 04:00 to something more appropriate for my morning routine. Let me adjust it to 8:00 AM.**Let me close the time picker and see what time it's set to now, then save the changes.**Good! The time has changed to 05:00 (5 AM), which is better than 04:00 but still earlier than I'd prefer. This is close enough for now though. Let me save these changes by looking for a "Done" or "Save" button in the navigation.**Perfect! There's a "Save" button in the top right. Let me tap it to save my changes.**Excellent! I'm back on the home screen and I can see my updated task: "✅ Take morning medication Daily 05:00 checkbox". The time has been successfully updated from 04:00 to 05:00.\*

_Let me take a moment to reflect on what I've accomplished during these two minutes of exploring:_

**What I've learned about Ting Mate:\***1. **Task Creation**: I successfully created a daily medication reminder2. **Voice Commands**: I discovered the voice interface with helpful examples3. **Editing**: I learned how to edit existing tasks and adjust their timing4. **Notifications**: I configured notification settings for task reminders and overdue alerts5. **Settings**: I explored accessibility options like text size and display modes\*

**How this app could help me:\***- **Medication Management**: Daily reminders ensure I don't forget my medications- **Voice Control**: When typing is difficult, I can use voice commands- **Sharing Features**: I could potentially connect with family members for additional support- **Customization**: The settings allow me to adjust the interface for my needs\*

_This app seems very well-designed for someone in my situation. The combination of simple task management, voice commands, notification reminders, and sharing capabilities could really help me maintain my independence while having the support I need on more challenging days._

_The interface is clean and intuitive, which is important for me. Even though I'm tech-savvy, having a simple, uncluttered design reduces cognitive load and makes it easier to use consistently._

</details>

<details>
<summary>Q2</summary>

Now please try to use a voice command to create a reminder.

(Note for you as Claude, not for the roleplaying persona):

Due to the limitation of this text-based chat, you cannot actually speak to perform voice input. Whenever your persona needs to use voice to perform an action, please just output the exact words your persona would say out loud. I will simulate the voice input on your behalf, then let you know what happens. After that, you can continue the task from there.

</details>

<details>
<summary>A2</summary>

Perfect! I've been wanting to try the voice command feature. It seems much more convenient than typing, especially when I'm having a day where fine motor control is more challenging. Let me activate the voice command interface first.\*_Great! The voice interface is active and it shows "I'm listening" at the bottom. I can see the helpful examples again. I want to create a reminder for something that's important to my routine - walking my dog. This is both good exercise for me and necessary for my dog's wellbeing. Let me speak my command:_

**"Remind me to walk my dog at 6 PM every day"**

</details>

<details>
<summary>Q3</summary>

continue

</details>

<details>
<summary>A3</summary>

_I just spoke my voice command and now I'm waiting to see how the app responds. This is exciting - if it works well, it could be so much easier than manually creating tasks, especially when I'm having difficulty with typing or remembering all the steps._

- Let me wait a moment to see what happens with my voice command for the dog walking reminder...\*_Wow! This is amazing! The app understood my voice command perfectly. I can see it's showing:_
- _My original command: "Remind me to walk my dog at 6pM Every day."The app's confirmation: "Okay! Should I create the task 'walk my dog' and remind you at 18:00?"Two clear options: "Yes" and "No"_

_This is exactly what I wanted! It correctly interpreted that I want a daily reminder to walk my dog at 6 PM (18:00 in 24-hour format). The voice recognition worked perfectly, and I love how it asks for confirmation before creating the task. This gives me a chance to make sure it understood correctly._

- The title "walk my dog" is perfect and concise. Let me confirm this by tapping "Yes".\*_Perfect! The voice command worked beautifully! I'm back on the main screen and now I can see both of my tasks:_

_1. **"✅ Take morning medication Daily 05:00 checkbox"** - my medication reminder2. **"📝 walk my dog Daily 18:00 checkbox"** - my new dog walking reminder_

_This is fantastic! I notice that the voice-created task has a different icon (📝 notepad) compared to my medication task (✅ checkmark), which helps distinguish between different types of tasks. The time is correctly set to 18:00 (6 PM), exactly as I requested._

_The voice command feature is incredibly intuitive and much faster than manually creating tasks. This would be especially helpful on days when I'm having difficulty with fine motor control or when I'm in a hurry. The natural language processing is excellent - it understood "6 PM every day" and converted it properly to the app's format._

_Now I have a complete daily routine set up:- Morning: Take medication at 05:00- Evening: Walk dog at 18:00_

_Both are set to repeat daily, and I've configured notifications so I'll get reminders. This gives me a solid foundation for managing my daily tasks. I could easily add more reminders for things like meals, exercise, appointments, or other medications using either the manual interface or the convenient voice commands._

_This app really seems designed with people like me in mind - those who need reliable reminders but want to maintain their independence and dignity._

</details>

### Stage 2: Using a pre-linked account after login

<details>
<summary>Q4</summary>

Have a look at the notes and find out where your key is.

</details>

<details>
<summary>A4</summary>

_Hmm, I'm not sure what you mean about notes and a key. I don't see any notes feature in this app that I've discovered yet, and I'm not sure what key you're referring to. Let me look around the interface to see if there's something I missed._

- Maybe there's a notes section I haven't found yet? Let me check if there are other features in this app I haven't explored. I'll look at the notifications button first to see if there's something there.\*_Oh! Perfect! I found the notes section! This appears to be a "Connect" or sharing view with various features including "Shared Notes." And there it is - I can see exactly what I was looking for:_

_Under "Shared Notes" there's a note that says:"Where things are - Glasses → on the small table by the couch- Remote → in the TV drawer_

- _Keys → on the hook by the front door"_

_Ah, my keys are on the hook by the front door! This is incredibly helpful. As someone with Alzheimer's, I sometimes forget where I put common items, and having this kind of reference note is invaluable. It looks like someone (maybe a family member if I was connected with "mates") has created this helpful list of where important items are kept in my home._

_This is exactly the kind of support feature that makes this app so valuable for people like me. Having a shared space where important information can be stored and accessed easily - like where things are kept - is a game-changer for maintaining independence while having the support I need._

_Now I know exactly where to find my keys when I need them! This shared notes feature could be used for so many helpful things like:- Emergency contact information- Important reminders about routines- Locations of important items (like this example)- Medical information- Appointment details_

_This really demonstrates how the "mate" sharing feature could work in practice to provide subtle but crucial support._

</details>

### Stage 3: Feedback

<details>
<summary>Q5</summary>

What part of the app do you like the most? And what you don't like the most?

</details>

<details>
<summary>A5</summary>

_After exploring this app for a bit, let me think about what's working well for me and what could be improved..._

**What I like most:**

_The voice command feature is absolutely my favorite part! Being able to just say "Remind me to walk my dog at 6 PM every day" and have it create the task perfectly is incredible. On days when my fine motor skills aren't as sharp or when I'm feeling overwhelmed, being able to just speak naturally instead of navigating through multiple screens is a huge relief. The fact that it understood my natural language and converted it correctly to the app's format shows really thoughtful design._

_I also love the shared notes feature I just discovered. Having that quick reference for "where things are" is invaluable for someone like me. Sometimes I forget where I put my keys or glasses, and having that information easily accessible gives me confidence and reduces anxiety._

**What I don't like the most:**

_The time picker is definitely my biggest frustration. When I was trying to set my medication reminder to 8 AM, I struggled with those sliders and ended up with 4 AM, then 5 AM - never quite getting to where I wanted. For someone who might have some dexterity challenges or cognitive load issues, those tiny sliders are really difficult to use precisely. I wish there was a simpler way to set times, maybe with larger buttons or a different interface altogether._

_I also found some of the navigation a bit confusing initially. The tutorial helped, but there were moments where I wasn't sure if I was in settings, or connect mode, or the main app. A clearer visual hierarchy or maybe some breadcrumbs would help me feel more oriented, especially on days when my cognitive load is higher._

**Overall though:**

_This app really feels designed with people like me in mind. The combination of simple task management, voice commands, sharing capabilities, and accessibility features like text size options shows a deep understanding of what we need to maintain our independence while having support when necessary. The voice feature alone could be life-changing for daily routine management._

</details>

<details>
<summary>Q6</summary>

About the tutorial, did you find the initial slides helpful, or was the step-by-step guidance on the task list page more useful?

</details>

<details>
<summary>A6</summary>

_That's a really thoughtful question! Looking back on my experience with both types of guidance..._

**The initial slides were good for setting expectations:**

_Those first slides with "Stay on Top of Your Day," "Use It Together," and "Stay Close, Even from Afar" gave me a nice overview of what the app could do. They helped me understand the bigger picture - that this wasn't just a simple reminder app, but something designed for sharing and support. That context was valuable before diving in._

**But the step-by-step guidance was much more helpful for actually learning:**

_The tutorial that showed me exactly where things would appear - "Tasks will show up here," "Tap here to add a task," "You can also edit tasks with your voice" - was infinitely more useful. It was contextual and showed me the actual interface I'd be using. For someone like me who might have some cognitive challenges, seeing the real buttons and areas while being guided through them made it stick much better._

_What made the step-by-step tutorial especially good was that it was progressive - it didn't overwhelm me with everything at once. Step 1: here's where tasks appear. Step 2: here's how to add them. Step 3: here's the voice option. That pacing worked really well for me._

**The one thing I found confusing:**

_I did get a bit confused when I tapped Settings and triggered what seemed like another tutorial sequence about text size and connecting mates. I wasn't sure if that was part of the original setup or if I had accidentally started something new. Some clearer labeling of "initial setup" vs "ongoing tutorials" would help._

**My recommendation:**

_Keep both, but maybe make the initial slides shorter and more focused on the key value proposition, then rely more heavily on the contextual, step-by-step guidance within the actual interface. For people with memory issues, learning by doing in the real interface is much more effective than abstract explanations._

</details>

<details>
<summary>Q7</summary>

Would you like to use this app with your relatives together?

</details>

<details>
<summary>A7</summary>

_That's such an important question for me to consider carefully..._

**My honest feelings are mixed:**

_On one hand, I can absolutely see the value. The shared notes feature we just looked at - with the reminder about where my keys are - shows how helpful it could be to have family members who can add important information I might forget. And knowing that someone could see if I've taken my medication or completed my daily walk could provide valuable peace of mind for both me and my loved ones._

**But I also have some concerns:**

_Independence is really important to me. At 50, with younger-onset Alzheimer's, I'm still very capable and want to maintain my autonomy as much as possible. I worry about feeling like I'm being monitored or watched constantly. There's a difference between having support available and feeling surveilled._

_The location sharing feature, for example, makes me a bit uncomfortable. I understand the safety rationale - if I get confused or lost, my family could find me. But right now, I'm still getting around just fine on my own, and I don't want to feel like I'm being tracked._

**How I might approach it:**

_I think I'd want to start slowly and selectively. Maybe begin by sharing just the task reminders with one trusted family member - perhaps my spouse or adult child - so they could see that I'm keeping up with my medication routine. That feels supportive rather than intrusive._

_The shared notes feature is something I'd definitely want to use together. Having my family help maintain lists of where things are, important phone numbers, or upcoming appointments would be incredibly helpful._

_But I'd want to maintain control over what gets shared and with whom. Maybe start with basic task sharing and see how it feels before adding location features or connecting with multiple family members._

**The key for me is dignity:**

_I want technology that helps me stay independent longer, not technology that makes me feel like I'm already losing my independence. This app seems like it could do both, depending on how it's used._

</details>

<details>
<summary>Q8</summary>

Are there any other features you’d like to see in this app?

</details>

<details>
<summary>A8</summary>

_That's a great question! Based on my experience with the app and thinking about my daily life with younger-onset Alzheimer's, there are several features that would make this even more helpful for me:_

**Photo-based reminders:\***Sometimes I struggle to remember what something looks like or where exactly it is. It would be amazing if I could attach photos to tasks or notes. For example, a photo of my medication bottles for the morning reminder, or a picture of the exact hook where my keys go. Visual cues are often more powerful than text for me.\*

**Emergency contact quick access:\***I'd love a prominent emergency button that could quickly call my doctor, family member, or emergency services if I'm feeling confused or disoriented. Sometimes I have moments where I'm not sure where I am or what I should be doing, and having that immediate access would be reassuring.\*

**Medication tracking with dosage reminders:\***The current reminder is great, but it would be helpful to track which specific medications I've taken and their dosages. Sometimes I can't remember if I already took my pills or not. A simple "mark as taken" feature with a visual confirmation would prevent double-dosing.\*

**Daily routine templates:\***It would be wonderful to have preset routines I could activate. Like a "morning routine" that includes medication, breakfast, and walking the dog, or an "evening routine" with dinner, dog walk, and preparing for tomorrow. On particularly difficult days, having a structured template would be very grounding.\*

**Voice notes feature:\***Sometimes I want to quickly record a thought or reminder when I'm not near the app or can't type. Being able to leave myself voice messages that I could listen to later would be incredibly useful.\*

**Simple calendar integration:\***I'd love to see my appointments and reminders in one place, maybe a simple week view that shows both my tasks and any medical appointments or social events.\*

_The core of what I'd want is anything that reduces cognitive load while maintaining my dignity and independence. This app is already quite thoughtful in that regard!_

</details>

<details>
<summary>Q9</summary>

Do you like the features on "Connect" screen?

</details>

<details>
<summary>A9</summary>

_Looking at the Connect screen more carefully, I have some nuanced feelings about these features..._

**What I appreciate:**

_The "Shared Notes" section is genuinely helpful - having that reference list of where my glasses, remote, and keys are located is exactly the kind of support I need. It's practical and unobtrusive. I can see how family members could add useful information here without it feeling invasive._

_I also like that there's a "Shared Space" option - the idea of having a common area for important information appeals to me. It feels collaborative rather than one-sided._

**What makes me more hesitant:**

_The "Mate's Location" feature gives me pause. While I understand the safety rationale - if I got confused or lost, my family could find me - it feels quite invasive at my current stage. I'm still navigating independently and don't want to feel like I'm being tracked constantly. Maybe this would be more appealing to me later if my condition progresses, but right now it feels like it assumes I'm less capable than I am._

_"Mates' Contacts" seems useful in theory, but I'm not sure I need a special interface for this - I already know how to reach my family members._

**The "Shared Logs" section concerns me a bit:**

_Right now it shows "No Log Found," but I'm wondering what kind of logs this would track. If it's logging my every movement or activity, that would feel too much like surveillance. However, if it's more like a shared diary or communication log with family members, that could be valuable._

**My overall feeling:**

_These features feel like they're designed for someone at a more advanced stage of memory impairment than where I am now. The shared notes are perfect for my current needs, but the location tracking feels premature. I'd prefer to ease into the sharing features gradually - maybe starting with just task sharing and notes, then adding location features only if and when I feel I need that level of support._

_The key for me is maintaining agency over what gets shared and when._

</details>
