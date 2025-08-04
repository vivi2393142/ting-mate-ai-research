# Participant Profile

- **Date**: 2025-08-04
- **Participant**: Jane
- **Role**: Care Receiver
- **Test Platform**: iOS Simulator via MCP (Claude Desktop)
- **Simulated Account**: [JaneT@gmail.com](mailto:JaneT@gmail.com) (linked with John – [JaneTMate@gmail.com](mailto:JaneTMate@gmail.com))

## Background

See Jane and her caregiver John in Set 2 – [Persona Profiles](personas_design.md)

## Execution Summary

### Stage 1: without login and linking

| #   | **Planned Prompt / Task**                                               | Execution                                                        | Completed | Notes                                                                |
| --- | ----------------------------------------------------------------------- | ---------------------------------------------------------------- | --------- | -------------------------------------------------------------------- |
| 1   | _"This app helps you remember daily things. Please explore it freely."_ | (No prompt)                                                      | Yes       | Completed naturally without any hint.                                |
| 2   | _(No prompt)_ — allow 2 minutes for free exploration                    | (No prompt)                                                      | Yes       | Completed naturally without any hint.                                |
| 3   | _"Try adding a task reminder, like ‘Take medicine tomorrow at 8am’."_   | (No prompt)                                                      | Yes       | Completed naturally without any hint.                                |
| 4   | _"Try using voice input to create a reminder."_                         | Due to technical limitation, simulated voice input via GPT text. | Yes       | Reminder created for doctor’s appointment, but recurrence was wrong. |

### Stage 2: with login and linking

| #   | **Planned Prompt / Task**                                            | Execution         | Completed | Description                                                           |
| --- | -------------------------------------------------------------------- | ----------------- | --------- | --------------------------------------------------------------------- |
| 5   | _"Assume you’ve just finish appointment with doctor, mark as done."_ | No further prompt | No        | Tapped into edit screen; misunderstood and deleted task instead.      |
| 6   | _"Have a look at the notes and find out where your key is."_         | No further prompt | Yes       | Located and read shared note naturally.                               |
| 7   | _"Try finding the contact list and making a call to John."_          | No further prompt | Yes       | Navigated correctly; actual call failed due to simulator environment. |

## Findings

### Strengths

| Category        | Summary                  | Description                                                                 | Supporting Quote                                                                                                                              |
| --------------- | ------------------------ | --------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Voice Input     | Highly accessible        | Simplified task creation and reduced cognitive load through natural speech. | _“Being able to just say "Remind me about my doctor's appointment on Friday at 10 AM" and have it understand me perfectly - that's amazing.”_ |
| Shared Notes    | Memory support           | Helped recall item locations and encouraged shared caregiving routines.     | _“That "Where things are" list that John left for me was incredibly helpful.”_                                                                |
| UI Clarity      | Easy to navigate         | User located main features and completed core tasks without confusion.      | _“This looks pretty straightforward!”_                                                                                                        |
| Shared Logs     | Confidence reinforcement | Helped reflect on accomplishments and reassured both user and caregiver.    | _“On days when my memory is foggy, I could look back and see that I did accomplish things.”_                                                  |
| Contextual Help | Step-based learning      | In-app guidance proved more effective than intro slides.                    | _“Step-by-step guidance was definitely more valuable.”_                                                                                       |
| Emotional Value | Collaborative feeling    | Felt supported rather than supervised; strengthened caregiver relationship. | _“It feels collaborative - like John and I are working together to help me stay independent.”_                                                |

### Areas for Improvement

| Category             | Short Summary             | Description                                                              | Supporting Quote                                                                                                          |
| -------------------- | ------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| Time Picker          | Difficult to operate      | Slider-based UI made accurate time input frustrating.                    | _“I tried several times to change my medication reminder from 12:00 to 8:00 AM, but I couldn't get it to work properly.”_ |
| Voice Input Accuracy | Misinterpreted recurrence | Voice-created reminder was accurate in time but incorrect in repetition. | —                                                                                                                         |
| Location Features    | Mixed emotional response  | Appreciated safety intent, but disliked being tracked.                   | _“I don’t want to feel like I’m being monitored all the time.”_                                                           |

## Evaluation Insights

Jane, a younger adult with early-onset dementia, completed most tasks independently. She found the onboarding, voice commands, and Connect features useful. While the app improved her confidence and gave her a sense of agency, she faced challenges with the time picker, recurrence rules, and completing tasks.

### **Recommendations**

- Simplify or replace time picker (e.g., presets like “Morning”, “Evening”).
- Improve recurrence rule detection in voice input.
- Make location features opt-in and clearly explained.
- Consider future features:

  - Attach photos to reminders (e.g., pills).
  - Mood check-in logs ("good day", "okay day", etc.).
  - Large emergency shortcut button.
  - Location-triggered reminders.

### **Test Method Notes**

This test used Claude connected to the iOS Simulator via `idb`, reading screen structure in JSON. Due to simulator limitations, features such as in-app calling or precise checkbox interaction could not be completed reliably.

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

_I settle into my chair and pick up the phone, looking at the screen with mild curiosity_

Oh, there's something new here. John must have put this on my phone for me. Let me see what this is all about._I look at the screen and read out loud_

"Ting Mate... Stay on Top of Your Day. Create simple reminders and check off tasks like medicine or appointments."

Oh, this looks like it might be helpful! It says something about reminders for medicine and appointments. That sounds like something John would want me to have. Let me see... there's a "Next slide" button here.

_I tap on the Next slide button**I try tapping the button again, making sure to use whole numbers**I watch as the screen changes\*\*I read the new screen_

"Use It Together... Share your tasks with a mate you trust, or connect to manage a mate's shared tasks."

Oh, this is interesting! It sounds like John and I could use this together. He's always trying to help me remember things, and this might make it easier for both of us. Let me continue and see what else it shows me.

_I tap the Next slide button again\*\*I read this new page_

"Stay Close, Even from Afar... Get alerts when your mate leaves a safe zone."

Hmm, this is about location alerts. I'm not sure how I feel about that. John already worries about me enough. But I suppose it could be helpful if I get confused when I'm out. Let me see what's next.

_I tap Next slide again\*\*I look at the screen and see two options_

Oh, now it's asking me how I plan to use it. I can see "Try It for Yourself" and "Connect with Mates". Since John and I would probably use this together, I think "Connect with Mates" makes more sense. Let me tap on that option.

_I tap on the "Connect with Mates" section\*\*I see the screen has a message about signing up_

"Sign up to connect with your mate and use all features."

I see there's a Skip and Next button. I'm not sure if I want to sign up right now - that seems like something John would want to help me with. Maybe I should skip this for now and just explore the app a bit more.

_I tap on the Skip button\*\*I look around the settings screen_

Oh good, I'm now in the app! I can see different sections like GENERAL, NOTIFICATION, CONNECT, and ACCOUNT. And there are buttons at the bottom - Connect, Home, and Settings. It looks like I'm currently on the Settings page.

Let me explore a bit. I notice it says "No mates yet? Tap here to get started" under the CONNECT section. But first, let me go to the Home screen to see what the main part of the app looks like.

_I tap on the Home button\*\*I see a mostly empty screen with a message_

"Tasks will show up here."

Oh, so this is where my reminders and tasks would appear. But it's empty right now since I haven't created any yet. There are Skip and Next buttons again - this must be part of another tutorial or walkthrough.

Let me tap Next to see if there's more to learn about how to use this._I read the instruction on screen_

"Tap here to add a task."

Oh, I see! This is showing me how to add tasks. This seems like it would be really helpful for me to remember things like taking my medication or appointments. Let me continue with the tutorial to learn more.

_I tap Next\*\*I read the text on the screen_

"You can also edit tasks with your voice."

Oh, that's interesting! Voice editing could be really helpful for me. Sometimes it's easier for me to just say what I need to remember rather than typing it all out. That sounds like a nice feature.

I see there's a "Finish" button now, so this must be the end of the tutorial. Let me tap that to finish learning about the app._I look at the main screen now that the tutorial is done_

Perfect! Now I can see the actual app. It says "Today's Tasks" at the top, and "You haven't added any tasks yet. Add a task to get started!"

I can see there's a big "Add Task" button, and there's also a round button at the bottom that says "Start Voice Command" - that must be for the voice feature they mentioned.

This looks pretty straightforward! Let me try adding a task. I should probably start with something simple, like reminding myself to take my medication. Let me tap on "Add Task"._I look at the form to add a new task_

Oh great! This is the "Add Task" screen. I can see different fields I need to fill out:

- Title: where it says "Add task title"
- Icon: shows a checkmark emoji
- Time: shows "14:00"
- Repeat: shows "Daily"

Let me start by adding a title for my medication reminder. I'll tap on the title field first._I clear the placeholder text and type my medication reminder\*\*I look at what I've typed_

Good! I've entered "Take morning medication" as the title. Now let me check what the current time setting is. It shows 14:00, but I usually take my medication in the morning around 8 AM. Let me tap on the time field to change it._I see that time pickers have appeared - sliders to set the hour and minute_

Perfect! I can see there are two sliders for setting the time. The current time is 14:00 (2 PM), but I want to set it to 8:00 AM for my morning medication. Let me adjust the hour slider first. I need to move it to 8 instead of 14._Let me try dragging the slider to change the hour**Let me check what time it shows now**I see it changed to 12:00. I need to get it to 8:00, so I need to swipe up more to decrease the hour**It's still showing 12:00. Let me try a longer swipe to get to 8:00**The time is staying at 12:00. Let me try tapping elsewhere to close the time picker and work with what I have for now. Maybe 12:00 isn't too bad - I can always adjust it later\*\*Good, I'm back to the main task creation form. I can see my task details so far:_

- Title: "Take morning medication" ✓
- Icon: checkmark emoji (that's fine)
- Time: 12:00 (not ideal, but workable for now)
- Repeat: Daily (perfect for medication)

The settings look pretty good! "Daily" repetition is exactly what I need for my medication reminder. Now I need to save this task. Let me look for a save or done button. I don't see one on the current screen, so maybe I need to scroll down or look for it in the navigation._Let me check the navigation bar to see if there are save or back buttons**Perfect! I found a "Done" button in the top right corner. Let me tap that to save my task.**I'm excited to see my task was created successfully!_

Oh wonderful! I can see my first task is now showing up under "Today's Tasks"! It shows "✅ Take morning medication Daily 12:00" with a checkbox. This is great - I've successfully created my first reminder!

Even though the time isn't perfect (12:00 instead of 8:00), having this daily medication reminder will be really helpful. John will be so pleased to see that I can use this app to help myself remember important things.

Let me explore a bit more. I'll try the voice command feature that they mentioned earlier - that round button at the bottom looks interesting._I look at the voice command interface with interest_

Oh this is neat! The voice command screen is showing me examples of what I can ask:

- "Remind me to take my pills at 2 every day"
- "Change my pill reminder to 4 p.m."
- "Can you delete the 'take medicine' task?"

And it says "I'm listening" at the bottom, which means it's ready for me to speak. This could be really useful! I can just talk to it instead of having to remember how to navigate through all the menus.

Actually, this gives me an idea - maybe I can use voice to fix the time on my medication reminder. Let me try saying something to change it to 8 AM.

_Speaking to the phone_ "Change my medication reminder to 8 AM."

_Since I can't actually speak in this test, let me close this for now and explore other parts of the app**I'm back to the main screen with my task visible. Let me check out the Connect tab to see what that's about, since the app mentioned connecting with mates**I see another tutorial screen about the Connect feature_

"See where you or your mates are here."

This looks like it's about location sharing - probably the feature they mentioned about getting alerts when someone leaves a safe zone. This could be useful for John to know where I am, especially if I get confused when I'm out. Let me continue with this tutorial._I read the next step in the tutorial_

"Add contact info for your mates."

This makes sense - I'd need to add John as my "mate" so we can share tasks and location information. This would be really helpful for both of us. Let me continue._I read the final tutorial step_

"Notes and logs for you and your mates."

So this section would show notes and logs that John and I can share. That could be really useful for him to keep track of how I'm doing or for me to leave notes about how I'm feeling or what I've done during the day.

Let me finish this tutorial._I look at the Connect screen with all its features_

Perfect! Now I can see the full Connect screen. There are three main sections at the top:

- "Mates' Contacts" (selected)
- "Mate's Location"
- "Shared Space"

And below that I see:

- "Shared Notes" (shows "No Note Found" with an add button)
- "Shared Logs" (shows "No Log Found")

This is really comprehensive! I can see how John and I could use this together. The shared notes would be great for us to communicate, and the logs might track our activities.

But since I don't have any mates connected yet, everything shows as empty. This is something I'll definitely want to set up with John's help later.

For now, I've gotten a good feel for this app! I successfully:

- Went through the onboarding tutorials
- Created my first task (medication reminder)
- Explored the voice command feature
- Learned about the Connect features for sharing with mates

This app seems like it could be really helpful for managing my daily routine and staying connected with John. The simple interface and voice commands would make it easy for me to use even when I'm having difficulty remembering things.

_I feel satisfied with my exploration of the app and am ready to show John what I've learned_

</details>

<details>
<summary>Q2</summary>

Now please try to use a voice command to create a reminder.

(Note for you as Claude, not for the roleplaying persona):

Due to the limitation of this text-based chat, you cannot actually speak to perform voice input. Whenever your persona needs to use voice to perform an action, please just output the exact words your persona would say out loud. I will simulate the voice input on your behalf, then let you know what happens. After that, you can continue the task from there.

</details>

<details>
<summary>A2</summary>

I want to try using the voice command feature to create another reminder. Let me go back to the Home screen first and then access the voice command.\*_Perfect! I'm back in the voice command interface. It shows "I'm listening" which means it's ready for me to speak. I can see the examples it gave me earlier. I want to create a reminder for my doctor's appointment that's coming up. Let me speak to it._

Remind me about my doctor's appointment on Friday at 10 AM.

</details>

<details>
<summary>Q3</summary>

continue

</details>

<details>
<summary>A3</summary>

I wait expectantly, looking at the phone screen to see what happens after I spoke my voice command. I'm curious to see if the app understood what I said and if it will create the reminder for my doctor's appointment.\*_I'm delighted to see the app understood my voice command!_

Oh wonderful! It worked! I can see it shows my voice command: "Remind me about my doctor's appointment on Friday at 10:00am."

And the app is asking for confirmation: "Okay! Should I create the task 'doctor's appointment' and remind you at 10:00?"

That's exactly what I wanted! It understood that I wanted a reminder about my doctor's appointment and got the time right - 10:00. This is so much easier than trying to navigate through all those menus and buttons. Let me confirm by tapping "Yes"._I'm thrilled to see that my voice command worked perfectly!_

Excellent! It worked beautifully! Now I can see both of my tasks on the "Today's Tasks" screen:

1. "📝 doctor's appointment 10:00" - the new one I just created with voice
2. "✅ Take morning medication Daily 12:00" - the one I created earlier manually

This is wonderful! The voice command feature made it so much easier and faster to create the reminder. I just said what I needed and the app understood me perfectly. It even picked a nice notebook emoji for the doctor's appointment, which is different from the checkmark for my medication.

This is exactly the kind of help I need! I can just speak naturally to add reminders instead of trying to remember how to navigate through all the buttons and menus. John is going to be so impressed when I show him how easily I was able to use this voice feature.

The app seems like it will be really helpful for keeping track of my appointments and daily tasks. I feel much more confident about managing my schedule with this kind of assistance!

</details>

### Stage 2: Using a pre-linked account after login

<details>
<summary>Q4</summary>

Assume you’ve just finish appointment with doctor, please mark it as completed.

</details>

<details>
<summary>A4</summary>

I've just returned from my doctor's appointment and I want to mark it as completed in the app. Let me look at my tasks and check off the doctor's appointment.\*_I can see my tasks and I want to mark the doctor's appointment as completed. I can see the "📝 doctor's appointment 10:00 checkbox" task. Let me tap on it to check it off._

Perfect! I can see my doctor's appointment task right there. The appointment went well and now I want to mark it as completed. I can see it says "checkbox" so I should be able to tap on it to check it off._Oh, I see that tapping on the task opened the "Edit Task" screen instead of just checking it off. I can see all the task details and there's a "Delete Task" button at the bottom. Since I completed the appointment, I could delete this task, but first let me see if there's a way to mark it as completed. Let me look for a back button or done button to get back to the main screen first._

Oh, I see that clicking on the task opened it for editing instead of just checking it off. I can see the task details - "doctor's appointment" at 10:00, set to "Once" which makes sense since it's not a recurring appointment.

Let me look for a way to get back to the main screen. I should look for a back button or close button._I can see there's a "Cancel" button on the left. Let me tap that to get back to the main screen, and then I'll try to figure out how to mark the task as completed.\*\*I'm back on the main screen with my tasks. Maybe I need to find the actual checkbox part of the task to check it off. Let me try looking for a specific checkbox area on the doctor's appointment task. Perhaps I need to tap on the left side where the checkbox might be._

Let me try tapping on the left side of the doctor's appointment task where the checkbox should be, rather than in the middle of the task._It opened the edit screen again. Since the appointment is completed and it was a one-time event, maybe I should just delete the task. That would make sense - once I've completed a one-time appointment, I don't need the reminder anymore. Let me tap on the "Delete Task" button._

I see it opened the edit screen again. Since this was a one-time appointment that I've now completed, maybe the best thing to do is delete this task. It makes sense - I don't need a reminder for an appointment that's already finished. Let me tap on "Delete Task"._Perfect! The app is asking me to confirm the deletion: "Are you sure you want to delete this task?" with Cancel and Delete options. Since I completed the doctor's appointment, I'll confirm the deletion._

Perfect! The app is asking me to confirm: "Are you sure you want to delete this task?"

Yes, I want to delete it since I've completed the appointment. Let me tap "Delete"._Excellent! The doctor's appointment task has been successfully deleted. Now I can see that only my daily medication reminder remains._

Perfect! The doctor's appointment task has been deleted successfully. Now I can see just my remaining task:

"✅ Take morning medication Daily 12:00"

That makes sense - since the doctor's appointment was a one-time event that I completed, deleting it was the right way to handle it. My daily medication reminder stays because it's a recurring task that I need every day.

I feel really good about how I managed this! I was able to:

1. Use voice commands to create the appointment reminder
2. Complete my appointment
3. Remove the completed task from my list

The app worked exactly as I hoped it would. The voice feature made it so easy to add the reminder, and removing completed tasks keeps my list clean and organized. John will be pleased to see how I'm managing my tasks and appointments so well with this app!

</details>

<details>
<summary>Q5</summary>

Have a look at the notes and find out where your key is.

</details>

<details>
<summary>A5</summary>

_I need to check the notes to find out where my key is. Let me look at the shared notes section. I remember seeing that in the Connect tab._

Oh, I need to check the notes for my key! Let me go to the Connect section where I saw the shared notes earlier._Perfect! I found the note about where things are, including my keys!_

Oh wonderful! I can see there's a shared note that says "Where things are" and it lists:

- Glasses → on the small table by the couch
- Remote → in the TV drawer
- Keys → on the hook by the front door

So my keys are on the hook by the front door! That's very helpful. John must have left this note for me so I can find things when I need them. This is exactly the kind of thing that would be really useful for me - having a place where we can both keep track of where important items are located.

I can also see in the Shared Logs section that it's been tracking my activity:

- "1:36 PM Jane deleted the task: 'doctor's appointment'"
- "1:34 PM Jane connected with John"
- "1:24 PM Jane created a task: 'doctor's appointment'"
- "1:16 PM Jane created a task: 'Take morning medication'"

This is really helpful! Now I know exactly where to find my keys - on the hook by the front door. This shared notes feature is going to be so useful for John and me.

</details>

<details>
<summary>Q6</summary>

Try finding the contact list in the app and making a call to John

</details>

<details>
<summary>A6</summary>

_I want to find John's contact information and call him. I remember seeing "Mates' Contacts" at the top of this Connect screen. Let me tap on that to see the contact list._

I want to call John and let him know how well I'm doing with the app! I can see "Mates' Contacts" at the top here. Let me tap on that to see if John's contact information is there._Perfect! I can see John's contact information with his phone number and options to call him._

Excellent! I found John's contact information! I can see:

"John +44 07493 939896 Call John Send WhatsApp to John"

There are options to "Call John" and "Send WhatsApp to John". I want to call him to tell him how well I'm doing with this app. Let me look for the "Call John" button and tap on it._I can see the contact card for John. Let me try tapping in the area where it says "Call John" to initiate the call.\*\*I see that tapping on John's contact opened the "Edit Quick Contact" screen instead of calling him. I can see his details here - Name: "John", Phone: "07493 939896", and Methods: "Phone, WhatsApp". Let me look for a way to get back and try to find the actual call button._

Oh, it opened the contact editing screen instead. I can see John's details here. Let me go back and try to find the actual call button. I need to look for a Cancel or Back button first._I see the Cancel button. Let me tap that to go back to the contacts list.**I'm back at the contacts screen. I can see John's contact with "Call John" and "Send WhatsApp to John" options. Let me try tapping more specifically on the "Call John" part. I need to tap more towards the right side where the action buttons would be.**I see there's an error message: "Failed to initiate call." This makes sense since this is a simulator and can't actually make real phone calls. Let me tap OK to dismiss the error._

Oh, I see there's an error message: "Failed to initiate call." That makes sense - this must be because we're in a test environment and it can't actually make real phone calls. Let me tap "OK" to dismiss this error.

</details>

### Stage 3: Feedback

<details>
<summary>Q7</summary>

What part of the app do you like the most? And what you don't like the most?

</details>

<details>
<summary>A7</summary>

_I reflect on my experience using the Ting Mate app, thinking about what worked well for me and what was challenging._

Well, after exploring this app, I have to say there are definitely parts I really love and some things that were a bit challenging for me.

**What I like the most:**

The voice command feature is absolutely wonderful! Being able to just say "Remind me about my doctor's appointment on Friday at 10 AM" and have it understand me perfectly - that's amazing. It's so much easier than trying to navigate through all those menus and remember which buttons to press. Sometimes when I'm having a difficult day with my memory, speaking is just more natural than trying to figure out complex interfaces.

I also really appreciate the shared notes feature with John. Having that "Where things are" note that tells me my keys are on the hook by the front door - that's exactly the kind of help I need! And I love that John and I can both see the same information. It makes me feel more connected to him even when he's at work.

**What I don't like the most:**

The time picker was really frustrating for me. I tried several times to change my medication reminder from 12:00 to 8:00 AM, but I couldn't get it to work properly. The sliders were confusing and didn't seem to respond the way I expected. For someone like me who sometimes has trouble with fine motor control or remembering exactly how interfaces work, that was quite discouraging.

Also, I was confused about how to mark tasks as completed. When I tapped on my doctor's appointment, I expected to be able to just check it off, but instead it opened the editing screen. It took me a while to figure out that I needed to delete the completed task instead. That wasn't very intuitive for me.

Overall though, I think this app could be really helpful for John and me once we get the hang of it. The voice feature especially gives me confidence that I can manage my reminders even on days when I'm struggling more with my memory.

</details>

<details>
<summary>Q8</summary>

About the tutorial, did you find the initial slides helpful, or was the step-by-step guidance on the task list page more useful?

</details>

<details>
<summary>A8</summary>

_I think carefully about the different tutorial experiences I had with the app._

That's a really good question! Now that I think about it, the two tutorial approaches were quite different and served different purposes for me.

**The initial slides were helpful for the big picture:**
Those slides at the beginning - about staying on top of your day, using it together with mates, and the location features - gave me a good overview of what the app could do. It helped me understand that this wasn't just a simple reminder app, but something John and I could use together. That was reassuring because I knew I wouldn't be managing everything on my own.

But honestly, at that stage, it was a bit abstract. I was still learning what the app was about, so phrases like "share tasks with a mate" didn't mean as much to me yet.

**The step-by-step guidance was much more practical:**
The tutorial that showed me exactly where to tap to add a task, and then explained about voice commands - that was incredibly useful! It was happening right in the context where I'd actually be using those features. When it showed me "Tap here to add a task" with the little numbered circles, I could immediately see what I needed to do.

The voice command tutorial was particularly helpful because it gave me specific examples like "Remind me to take my pills at 2 every day" - that made it clear exactly how to talk to the app.

**What worked best for me:**
As someone with memory challenges, the contextual, step-by-step guidance was definitely more valuable. It's one thing to be told "you can add tasks" and another to be shown exactly how to do it when you're looking at the actual screen.

I think for people like me, learning by doing - right there in the real interface - sticks better than trying to remember abstract concepts from slides I saw earlier.

The initial slides were nice for getting excited about the possibilities, but the hands-on guidance is what actually taught me how to use the app.

</details>

<details>
<summary>Q9</summary>

Would you like to use this app with your relatives together?

</details>

<details>
<summary>A9</summary>

_I pause thoughtfully, considering how this app might work with John and potentially other family members._

Oh, absolutely! I think this could be wonderful for John and me to use together. In fact, I'm already excited to show him what I've learned today.

**With John especially:**
What I love is that John could help me set up reminders when I'm having trouble, and I can still manage them myself on better days. The shared notes feature where he left that helpful list about where things are - that's exactly what we need! He's always trying to help me remember where I put things, and now we have a place where we can both keep track.

And the activity logs that show when I create or complete tasks? That would give John some peace of mind when he's at work. He worries about me so much, especially since I restarted my medication. Being able to see that I took my medication or completed my appointments would help him feel less anxious.

**With our son:**
Our son visits once a month and he's the one who usually helps us with technology. I think he'd be really pleased to see us using an app like this successfully! He could help us set up more complex features or troubleshoot if we run into problems.

**What makes it special:**
What I really appreciate is that this doesn't make me feel like I'm being "managed" or watched over. It feels collaborative - like John and I are working together to help me stay independent. The voice commands especially make me feel capable and in control.

Sometimes I worry about being a burden on John with all my memory issues. But this app could actually make things easier for both of us. He wouldn't have to constantly remind me about things, and I'd have the support I need without feeling helpless.

I think apps like this could really help families like ours stay connected and supportive without anyone feeling overwhelmed or dependent.

</details>

<details>
<summary>Q10</summary>

Are there any other features you’d like to see in this app?

</details>

<details>
<summary>A10</summary>

_I think carefully about my daily challenges and what would make the app even more helpful for someone like me._

Oh, there are definitely some features that would make this app even better for people like me! Let me think about what would really help...

**Photo reminders:**
Sometimes I forget what my pills look like, or I can't remember if I already took them. It would be wonderful if I could take a photo of my medication bottle and attach it to my reminder. That way, when the reminder pops up, I'd see exactly which pills to take. John could even take photos of where important things are kept - like showing me the hook by the front door where my keys go.

**Simple daily check-ins:**
Some days I feel really good and clear-minded, other days are more foggy. It would be helpful to have a simple way to log how I'm feeling each day - maybe just "good day," "okay day," or "difficult day." Then John could see patterns and know when I might need extra support, and I could look back and see that bad days don't last forever.

**Emergency contacts that are really obvious:**
While the contacts are nice, in a real emergency I might panic and forget how to navigate to them. Maybe a big, bright "CALL JOHN" button right on the main screen that I could tap even when I'm confused or scared.

**Medication tracking that's more visual:**
Instead of just a reminder, what if there was a simple way to mark "taken" with a big checkmark, and maybe it could show me the last few days so I can see if I missed any doses? Sometimes I honestly can't remember if I took my morning pills.

**Location reminders:**
Since the app has location features, it would be amazing if it could remind me of things when I'm in certain places. Like reminding me to buy milk when I'm near the grocery store, or reminding me to take my evening medication when I get home.

**Simpler time setting:**
That time picker was really frustrating! Maybe just having preset times like "Morning," "Afternoon," "Evening" or being able to type in the time would be easier for people like me.

These features would really help me feel more confident and independent while still keeping John involved and informed.

</details>

<details>
<summary>Q11</summary>

Do you like the features on "Connect" screen?

</details>

<details>
<summary>A11</summary>

_I think about my experience with the Connect screen and its various features._

The Connect screen has some really thoughtful features, but I have mixed feelings about different parts of it.

**What I really like:**

The **Shared Notes** feature is fantastic! That "Where things are" list that John left for me was incredibly helpful. Being able to have a place where we both can leave information for each other feels very practical and supportive. I can imagine using this for so many things - shopping lists, reminders about appointments, or even just little encouraging notes to each other.

The **Shared Logs** are also reassuring in a way. I like that it tracks my activities - "Jane created a task," "Jane deleted a task" - because it gives both John and me a record of what I've been doing. On days when my memory is foggy, I could look back and see that I did accomplish things. And it helps John see that I'm managing well without him having to ask me directly, which preserves my dignity.

**What makes me a bit uncomfortable:**

The **location sharing** features... I'm honestly torn about this. I understand why it could be helpful - if I get confused when I'm out, John could find me. And the "safe zone" alerts might give him peace of mind when he's at work.

But there's also something that feels a bit... watched? I'm only 51, and I still drive and go places on my own. I don't want to feel like I'm being monitored all the time. It might make me feel more like a patient than a partner.

**The contact list is practical:**
Having John's contact information easily accessible is really useful, even though the actual calling didn't work in the test. In a real emergency, having that right there would be valuable.

**Overall thoughts:**
I think the Connect features could be wonderful for couples like John and me, but they need to be used thoughtfully. The shared notes and logs feel collaborative and supportive. The location features might be better as something we discuss and agree on together, rather than something that just runs automatically.

The key is that these features should help us stay connected and support each other, not make me feel like I'm being supervised.

</details>

<details>
<summary>Q12</summary>

Would you like to do "call your John" in this app, or you prefer your own way to do so?

</details>

<details>
<summary>A12</summary>

_I think about how I normally call John and compare it to the app's calling feature._

That's a really interesting question! After trying the calling feature in the app, I think I have some mixed feelings about it.

**What I liked about the app's calling feature:**
Having John's number right there in the app was convenient, especially since I was already using the app. I didn't have to remember his number or go hunting through my regular phone contacts. And I could see it was specifically set up for our caregiving relationship - it even had WhatsApp as an option, which we do use sometimes.

**But honestly, I think I prefer my own way:**
When I need to call John, I usually just use my regular phone the way I always have. I know where his contact is, and it feels more natural to me. I've been calling him the same way for years, and that routine is comfortable and familiar.

**The real value might be for emergencies:**
Where the app's calling feature could be really valuable is if I'm confused or panicked. If I'm having a particularly difficult day with my memory, or if I'm lost or scared, having that big obvious way to reach John right in the app I'm already using could be a lifesaver. I might not remember how to navigate to my regular phone contacts if I'm really distressed.

**My ideal scenario:**
I think I'd probably keep calling John the normal way for everyday conversations - like "How was your day?" or "What should we have for dinner?" But having the emergency contact feature in the app as a backup would give me confidence. It's like having a safety net that I hope I never need to use, but I'm glad it's there.

It's similar to how I feel about a lot of assistive features - I want them available when I need them, but I don't want to feel like I _have_ to use them for everything. I still want to maintain my normal routines and independence as much as possible.

</details>
