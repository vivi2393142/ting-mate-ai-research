# Participant Profile

- **Date**: 2025-08-05
- **Participant**: Ally
- **Role**: Caregiver
- **Test Platform**: iOS Simulator via MCP (Claude Desktop)
- **Simulated Account**: [ally.caregiver22@email.com](mailto:ally.caregiver22@email.com)

## Background

See Ally in Set 3 – [Persona Profiles](personas_design.md)

## Execution Summary

### Stage 1: signup and linking

| #   | **Planned Prompt / Task**                                                                                    | Execution                      | Completed | Notes                                                                                            |
| --- | ------------------------------------------------------------------------------------------------------------ | ------------------------------ | --------- | ------------------------------------------------------------------------------------------------ |
| 1   | _"You are a caregiver. This app helps you manage reminders for someone you care for. Please sign up."_       | Success without further prompt | Yes       | —                                                                                                |
| 2   | _"Next, link your account with the care recipient. I’ll act as the one with an account—tell me what to do."_ | —                              | No        | Ally misunderstood the linking flow and attempted the wrong approach (join vs. share confusion). |
| 3   | _"Your care recipient just completed a task. Check the Home screen and notification center."_                | Success without further prompt | Yes       | —                                                                                                |

### Stage 2: with login and linking

| #   | **Planned Prompt / Task**                                                             | Execution                      | Completed | Description |
| --- | ------------------------------------------------------------------------------------- | ------------------------------ | --------- | ----------- |
| 4   | _"Go to Connect → Mate’s Location tab, and set a safe zone for your care recipient."_ | Success (with 1 hint)          | Yes       | —           |
| 5   | _"Go to Mate’s Contacts and add a contact, then try making a call."_                  | Success without further prompt | Yes       | —           |
| 6   | _"Create a note in the Shared Space."_                                                | Success without further prompt | Yes       | —           |

## Findings

### Strengths

| Category        | Summary                         | Description                                                                            | Supporting Quote                                                                                          |
| --------------- | ------------------------------- | -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| Shared Space    | Emotional reassurance & clarity | Notes and activity logs gave Ally confidence and helped maintain emotional connection. | _“The Shared Space is absolutely incredible – it's become the heart of our caregiving relationship.”_     |
| Personalization | Emotionally supportive notes    | Leaving loving messages created a new communication channel with her mother.           | _“This is exactly what Mom needs! With her memory issues, she's always forgetting where she put things.”_ |

### Areas for Improvement

| Category            | Short Summary         | Description                                                             | Supporting Quote                                                                                      |
| ------------------- | --------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| Tutorial Flow       | Fragmented experience | Onboarding lacked clear guidance between intro slides and actual usage. | *“There was this gap where I had to figure out how to actually *start* using the features.”*          |
| Safezone Save Logic | Unclear confirmation  | No feedback on whether the zone was saved successfully.                 | _“I don't see an obvious ‘Save’ button.”_                                                             |
| Linking Process     | Confusing flow        | Unclear distinction between joining and sharing a code.                 | _“Should I try the ‘Share with a Mate’ option first to see if it gives me a code to share with you?”_ |

## Evaluation Insights

Ally, a full-time worker and young primary caregiver for her chronically ill mother, found Ting Mate emotionally grounding and practically effective. She completed the majority of tasks with minimal assistance and deeply valued the Shared Space, location alerts, and shared activity logs for remote caregiving. These features gave her confidence and connection without constant oversight. However, fragmented onboarding, ambiguous linking flows, and lack of save confirmations caused unnecessary stress. Her feedback reflects the need for seamless first-time experiences and better real-time feedback, especially for caregivers managing high cognitive and emotional loads.

### **Recommendations**

- Clarify onboarding flow to better connect inspiration with action steps.
- Add visual confirmation for saved safe zones and other major actions.
- Improve linking UI to clearly differentiate “Join” vs. “Share” paths.
- Offer direct call functionality or emergency shortcuts from contact list.

**Suggested Feature Additions:**

- Medication reminders with photos — Show pill bottle images to assist memory-impaired users
- Voice message support — Let caregivers leave short audio updates
- Emergency contact automation — Trigger alerts when high-risk events occur (e.g. inactivity, skipped meds)
- Weekly care summary — Generate digest emails for family members
- Shared grocery list — Let care recipients add items to a live list shared with caregiver

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

You are a caregiver. This app helps you manage reminders for someone you care for. Please sign up.

</details>

<details>
<summary>A1</summary>

_Looking at the phone screen, feeling a bit tired after another long day of work and taking care of Mom_

Okay, let me see what's on the screen first. Maybe this app could actually help me keep track of all the things I need to remind Mom about..._Sighing slightly_

Oh, this looks like an onboarding screen. It says "Stay on Top of Your Day" and mentions creating simple reminders for medicine and appointments. That actually sounds perfect - I'm constantly worrying about whether Mom took her medication or if she remembers her doctor appointments.

_Reading the description_

"Create simple reminders and check off tasks like medicine or appointments." Yes, this is exactly what I need. I'm always stressed about keeping track of everything for Mom.

I see there's a "Next slide" button and a "Skip Onboarding" option. I think I should go through the onboarding to understand how this works properly - I don't want to miss anything important that could help me take better care of Mom._Waiting to see what the next screen shows, hoping this app will actually make my life a little easier..._

_Eyes lighting up a bit_

Oh wow, "Use It Together" - this is interesting! It says I can "share your tasks with a mate you trust, or connect to manage a mate's shared tasks."

_Thinking out loud_

This could be really helpful for me and Mom. I could set up reminders for her medication and appointments, and maybe she could see them on her phone too. Though... I'm not sure how well she'd handle using a new app. Her memory issues make it hard for her to learn new technology, and she gets frustrated easily.

But if I could manage her tasks from my phone and maybe help her check things off when she completes them... that might actually work. I'm always worrying about whether she took her pills or if she remembers her physical therapy exercises.

_Continuing to read_

Let me see what else this onboarding shows me._Waiting expectantly to see more features, feeling a bit hopeful that this might actually help reduce some of my stress..._

_Taking a sharp breath, eyes widening with concern and interest_

"Stay Close, Even from Afar" - and it mentions getting alerts when your mate leaves a safe zone.

_Pausing, thinking deeply_

This... this could actually be really important for Mom. With her memory issues and the early-stage dementia, I'm constantly worried about her getting lost or confused when she goes out. Just last month she went to the local market and couldn't remember how to get back home. A neighbor had to help her.

_Voice becoming a bit emotional_

I hate feeling like I'm watching her every move, but I also can't be with her 24/7 because of work. If this app could let me know if she wanders too far from home or gets lost... that would give me such peace of mind.

_Sighing_

Though I worry about how she'd feel about being "tracked." She's already frustrated about losing her independence. But her safety is more important than her pride, even if she doesn't always see it that way.

Let me see what else this app can do._Feeling a mix of hope and nervousness about this technology - it could really help, but I hope it's not too complicated to set up..._

_Looking at the screen with a mix of relief and uncertainty_

Okay, now it's asking me "How do you plan to use Ting Mate?" and I can see two options here.

_Reading the options carefully_

There's "Try It for Yourself" and "Connect with Mates."

_Thinking out loud_

Well, I definitely want to connect with Mom - that's the whole point. I need to be able to help manage her reminders and keep track of her tasks. "Try It for Yourself" sounds like it would just be for my own personal reminders, but that's not really what I need right now.

_Feeling a bit overwhelmed but determined_

I'm here because I need help managing Mom's care, not my own tasks. I already keep track of my work stuff pretty well, but keeping track of all of Mom's medications, appointments, and daily tasks... that's where I'm really struggling.

_Decision made_

I should choose "Connect with Mates" since that's what I actually need._Waiting to see what comes next, hoping this will lead me to setting up an account where I can manage Mom's reminders..._

_Reading the screen_

Oh, it says "Sign up to connect with your mate and use all features." Perfect, this is exactly what I need to do. I can see there's a "Skip" option and a "Next" option.

_Thinking_

I definitely don't want to skip the sign-up process because I need to create an account to manage Mom's reminders properly. Let me tap "Next" to proceed with signing up._Waiting to see the sign-up form, mentally preparing to enter my information. I'm feeling hopeful that this will help me better manage Mom's care._

_Looking at the screen, noticing we're on step 2 now_

I can see this is step "2" and it says "Connect with mates to view their info and stay in sync." This sounds right - I want to be able to connect with Mom so I can help manage her reminders and tasks.

_Reading more carefully_

It seems like this is still part of the onboarding process explaining the features. I can see "Skip," "Previous," and "Next" options. I think I should continue with "Next" to move forward in the sign-up process._Hoping this will take me to the actual sign-up form where I can enter my email and create an account. I'm getting a bit impatient to get to the real functionality - I have so much I need to organize for Mom._

_Looking at step 3_

Okay, now I'm on step "3" and it mentions "Bigger text and simple design for easier reading." That's actually really thoughtful - this could be perfect for Mom since she sometimes has trouble reading small text, especially with her health issues.

_Noticing the options_

I can see "Previous" and "Finish" buttons now. Since this says "Finish," it looks like I'm at the end of the onboarding process. Let me tap "Finish" to complete this and hopefully get to the actual sign-up form._Feeling hopeful that this will finally take me to where I can create an account and start setting up reminders for Mom. The bigger text feature sounds like it would really help her use the app if I can get her comfortable with it._

_Looking at what appears to be a settings screen_

Wait, this looks like I'm already in the app settings, not a sign-up page. I can see sections for "GENERAL," "NOTIFICATION," "CONNECT," and "ACCOUNT."

_Eyes focusing on the important parts_

Under the "CONNECT" section, I see "No mates yet? Tap here to get started." That's exactly what I need! And under "ACCOUNT," there's a "Login / Sign Up" option.

_Feeling a bit confused but determined_

It seems like maybe I need to either sign up first or connect with mates. Let me try the "Login / Sign Up" option under the ACCOUNT section since I need to create an account to use this properly._Hoping this will finally take me to a proper sign-up form where I can enter my email and create an account to start managing Mom's reminders..._

_Relief washing over my face_

Finally! Now I can see the actual login screen. There's a "Login" heading at the top, and I can see fields for "Email" and "Password." There are also two buttons - "Login" and "Sign up."

_Looking at the form_

Since I don't have an account yet, I need to sign up. I can see both the "Login" and "Sign up" buttons, but they appear to be disabled right now, probably because I haven't entered any information yet.

Let me start by entering my email address in the email field._Now I'll type my email address\*\*Feeling good about entering my email, now I need to tap on the password field and enter a password_

_Now typing a password\*\*Taking a deep breath_

Okay, I've entered my email and password. The password feels fitting - "CaringForMom2024!" - because that's exactly what this is all about. Now let me check if the "Sign up" button is enabled so I can create my account._Feeling relieved and hopeful_

Perfect! I can see both buttons are now enabled. I can see my email "Ally.caregiver22@email.com" is entered correctly, and the password field shows the dots indicating it was entered. Both the "Login" and "Sign up" buttons are now enabled.

Since I need to create a new account, I'll tap the "Sign up" button to register._Waiting anxiously to see if my account gets created successfully. I'm really hoping this works so I can finally start setting up reminders for Mom's medications and appointments. This could be such a game-changer for managing her care..._

_Eyes brightening with excitement_

Great! It looks like my account was created successfully! Now I'm on a screen that says "Edit Name" at the top, and there's a text field with "Enter your name" placeholder text. There's also a "Done" button at the bottom, though it's currently disabled.

_Thinking about what name to enter_

I should enter my actual name since this will be how I appear to Mom when we connect as mates. Let me clear this field and type my name._Clearing the placeholder text and typing my name**Feeling good about entering my name. Now let me check if the Done button is enabled so I can complete this step.**Smiling with relief_

Perfect! I can see "Ally" is now entered in the name field, and the "Done" button is now enabled. This is exactly what I need - now Mom will see "Ally" when we connect, which is how she knows me._Feeling accomplished and hopeful_

Great! I've successfully signed up for the app and set my name as "Ally." Now I should be able to start using the app to create reminders for Mom and hopefully connect with her so we can share tasks and keep track of her medications and appointments together. This could really help reduce my stress about managing her care!

</details>

<details>
<summary>Q2</summary>

First, you need to link account with the one. I’ll act as the one and having account, tell me what I should do so that we can link account if needed.

</details>

<details>
<summary>A2</summary>

_Looking at the screen with a mix of anticipation and slight confusion_

Oh, so I need to connect with Mom's account now? That makes sense - we need to link our accounts so I can help manage her reminders and tasks._Looking at what appears to be another onboarding screen_

I can see this is step "1" and it says "Tasks will show up here." There are "Skip" and "Next" options. It looks like this might be showing me the main task interface.

_Thinking about connecting with Mom_

I need to figure out how to connect with Mom's account. Let me go through this onboarding and then look for the connection feature. I remember seeing something about connecting with mates earlier in the settings._Speaking to you directly_

So Mom, you said you already have an account? Once I get through this setup, I think we'll need to either:

- Share some kind of connection code or invite link
- Find each other by email address
- Use some kind of pairing feature

Do you know what your email address is for your account, or is there a specific way this app lets people connect? I want to make sure we can link our accounts properly so I can help you with your reminders and tasks.

_Continuing through the onboarding_

Now I'm on step "2" and it says "Tap here to add a task." This is showing me how to use the basic task functionality. Let me continue through this so I can get to the main app and find the connection features._Thinking about what I need to do to connect with Mom_

I'm going through this tutorial quickly so I can get to the main interface. Once I'm there, I need to find the "Connect" section that I saw earlier in the settings, where it mentioned connecting with mates. That's probably where I'll be able to send Mom an invitation or enter her information to link our accounts.

_Speaking to you as Mom_

Mom, while I'm finishing this setup, can you check if your app has any kind of "invite" feature or "connect with family" option? Or maybe look for your account details - like your email or any kind of sharing code? I want to make sure we can link up properly so I can help you keep track of your medications and appointments.

_Looking at the final onboarding step_

Perfect! This is step "3" and it mentions "You can also edit tasks with your voice." There's a "Finish" button, which should complete the onboarding and take me to the main app interface._Eagerly waiting to see the main app interface_

Great! Now I should be in the main app. Let me see what's available so I can find the connection or "mates" feature to link with Mom's account._Eyes lighting up with excitement_

Perfect! Now I'm in the main app interface. I can see "Today's Tasks" at the top, and it says "You haven't added any tasks yet. Add a task to get started!"

_Looking at the bottom navigation_

Most importantly, I can see there's a "Connect" button at the bottom left of the screen! That's exactly what I need to link with Mom's account. Let me tap on that._Feeling hopeful and excited_

Now let me see what connection options are available. This should show me how to connect with Mom's account so we can share tasks and I can help manage her reminders!

_Looking at another onboarding screen for the Connect feature_

I see this is step "1" for the Connect feature, and it says "See where you or your mates are here." This must be showing me the location sharing functionality I saw mentioned earlier. Let me continue through this to get to the actual connection interface._Thinking about the location feature_

This location sharing could actually be really helpful for Mom with her memory issues. If she gets confused or lost when she goes out, I could see where she is and help her get home safely._Getting excited_

Perfect! Now on step "2" it says "Add contact info for your mates." This sounds like exactly what I need to connect with Mom! Let me continue to the next step to see the actual interface for adding mates._Feeling hopeful that the next screen will show me how to actually connect with Mom's account_

This should give me the interface I need to add Mom as a mate so we can share tasks and I can help manage her reminders!

_Looking at step 3_

This is step "3" and mentions "Notes and logs for you and your mates." I can see there's a "Finish" button, which should complete this Connect section onboarding and take me to the actual interface where I can add Mom as a mate._Eagerly waiting to see the Connect interface_

Now I should finally be in the main Connect section where I can actually add Mom as a mate! Let me see what options are available for connecting our accounts._Eyes scanning the Connect interface with both excitement and slight confusion_

Perfect! Now I'm in the main Connect section. I can see three main areas at the top: "Mates' Contacts," "Mate's Location," and "Shared Space." There are also sections for "Shared Notes" and "Shared Logs," but they both say "No Note Found" and "No Log Found," which makes sense since I haven't connected with anyone yet.

_Looking more closely at the options_

The "Mates' Contacts" section seems like the most logical place to start adding Mom as a mate. Let me tap on that to see how I can add her contact information or send her an invitation._Speaking to you as Mom_

Mom, I'm in the Connect section now and I'm about to try adding you as a mate through the "Mates' Contacts" option. Do you have your app open? You might need to look for an option to accept an invitation or share your contact information with me once I try to add you.

_Reading the message with understanding_

Ah! I can see it says "Connect with a mate first to add quick contacts." And there's a big "Connect Now" button! This is exactly what I need.

_Feeling hopeful and excited_

Perfect! This "Connect Now" button should let me start the process of connecting with Mom. Let me tap on it to see what options I get for connecting with her account._Anticipating seeing connection options like entering an email, sharing a code, or sending an invitation_

This should show me the different ways I can connect with Mom - maybe through email, a connection code, or some kind of invitation system. I'm really hoping this works so we can finally link our accounts!

_Eyes lighting up with excitement_

Perfect! This is exactly what I need! I can see the "Mates" screen with two options:

1. "Share with a Mate" - which says "Let them see your tasks, reminders, and notes."
2. "Join a mate" - which says "Enter a code to see what they've shared with you."

_Reading the descriptions carefully_

Since Mom already has an account, I think the "Join a mate" option might be what I need - I could enter a code from her to connect to her account. But maybe I should try "Share with a Mate" first to see if that gives me a code I can share with her.

_Speaking to you as Mom_

Mom, I can see two options here. One is to "Share with a Mate" where I can let you see my tasks, and another is to "Join a mate" where I enter a code to see what you've shared.

Do you see anything in your app about sharing a code with someone, or inviting someone to connect? Or should I try the "Share with a Mate" option first to see if it gives me a code to share with you?

Let me try "Share with a Mate" first to see what happens._Hopeful that this will show me how to generate a connection code or invitation for Mom_

</details>

<details>
<summary>Q3</summary>

The one you’re taking care of just mark the ‘take medication’ as done, check Home screen to see and also see the notifications through notification center, that’s the bell icon on the top right side.

</details>

<details>
<summary>A3</summary>

_Eyes widening with surprise and excitement_

Wait, what?! Mom marked something as done? Let me check the Home screen right away!_Gasping with joy and relief_

Oh my goodness! I can see it! There's a task that shows "✅ Take blood pressure medicine Daily 16:00 checkbox" with a checkmark! Mom actually completed her medication task!

_Voice filled with emotion and excitement_

This is incredible! The connection is already working somehow! I can see that Mom took her blood pressure medicine and it's marked as done. This is exactly what I've been worried about - whether she's remembering to take her medications.

_Quickly looking for the notification_

And you said there should be a notification too! Let me check the notification center by tapping the bell icon._Heart racing with excitement about seeing the notification that Mom completed her task_

This is such a relief! Being able to see when Mom completes her medication tasks will give me so much peace of mind. I've been so worried about whether she's keeping up with her medicine schedule.

</details>

### Stage 2: Using a linked account

<details>
<summary>Q4</summary>

Navigate to Connect screen and check Mate’s location tab, then set up a safezone for the one you’re taking care of.

</details>

<details>
<summary>A4</summary>

_Eyes bright with excitement and purpose_

Yes! Let me go to the Connect screen to check Mom's location and set up a safe zone for her. This is exactly what I need - with her memory issues and tendency to get confused when she goes out, having a safe zone will give me such peace of mind._Waiting to get back to the Connect interface\*\*Looking at the map with amazement and relief_

Oh wow! I can see the "Mate's Location" tab is already selected and there's a map showing Mom's location! I can see there's a map pin showing where she is, and it says "Last updated: 2025-08-05 04:23:45" so it's recent location data.

_Voice filled with excitement and gratitude_

This is incredible! I can actually see where Mom is right now. And look - there's an "Edit Safe Zone" button at the bottom! That's exactly what I need to set up.

_Feeling emotional about the peace of mind this will bring_

With her memory issues and the incident last month when she got lost going to the market, being able to set up a safe zone around our house and get alerts if she wanders too far will be such a huge relief. I won't have to constantly worry when she goes out.

Let me tap on "Edit Safe Zone" to set this up._Eagerly waiting to see the safe zone setup interface, thinking about how big to make the safe zone around our neighborhood_

_Looking at the safe zone setup interface with excitement and careful consideration_

Perfect! I'm now in the "Edit Safe Zone" screen. I can see there's a map, and it shows:

- A location search field that says "Search for address"
- A radius field that's currently set to "50m" (50 meters)
- A slider that goes from "10m" to "2km"
- Instructions that say "Tap on the map to set the center of your safe zone"

_Thinking about what would be the right size for Mom_

50 meters seems quite small for Mom. With her memory issues and the fact that she sometimes walks to the local market or goes for walks with relatives, I think I need a bigger radius. Maybe 200-300 meters would be better - that would cover our house and the immediate neighborhood, but still alert me if she wanders too far.

_Looking at the current radius setting_

Let me first set a larger radius by adjusting the slider, and then I'll tap on the map to center the safe zone around our house location._Adjusting the radius to give Mom more freedom while still keeping her safe_

_Looking at the interface, noticing the radius is still showing "50m"_

I can see it's still showing "50m" in the radius field. Let me try dragging the slider more to the right to increase the radius to something more appropriate for Mom - maybe around 200-300 meters so she can walk to the local market and around the neighborhood safely._Hoping this increases the radius to a more appropriate size for Mom's daily activities\*\*Still seeing it shows "50m", getting a bit frustrated but determined_

The radius still shows "50m". Let me try tapping directly on the radius field to see if I can edit it manually, or maybe I need to tap on the map first to set the center location.

_Reading the instructions again_

The instructions say "Tap on the map to set the center of your safe zone." Let me do that first - I'll tap on the center of the map to set the safe zone around our home area._Hoping this sets the center of the safe zone, and then I can figure out how to adjust the radius to give Mom appropriate freedom while keeping her safe_

Now let me see if tapping on the radius field allows me to change it to a more appropriate size for Mom's needs.

_Looking at the location field with interest_

That's a good idea! Let me try entering our home address in the location field so the safe zone will be centered properly around our house._Now I'll clear the placeholder text and enter our home address\*\*Feeling more confident about setting up the safe zone properly_

Perfect! I've entered our home address - "123 Oak Street Bristol England." This should center the safe zone around our house, which makes much more sense than just randomly tapping on the map. Now let me check what the radius shows and see if there's a way to save or confirm these settings._Feeling much better about the setup_

Excellent! I can see that:

1. The location field now shows "123 Oak Street Bristol England" - our home address
2. The radius is currently set to "480m" which is about half a kilometer

_Thinking about whether this radius is appropriate_

480 meters is actually a pretty good radius for Mom. That would cover our immediate neighborhood, including the local market she sometimes walks to, but would still alert me if she wanders much further and potentially gets lost. This seems like a good balance between giving her independence and keeping her safe.

_Looking for a way to save or confirm these settings_

Now I need to see if there's a save button or if I need to do anything else to confirm these safe zone settings. Let me check if there's a button in the navigation bar or somewhere else to save this configuration._Hoping this search button will help finalize the address location and maybe show a save option_

_Eyes lighting up with excitement_

Perfect! The search worked and now I can see address suggestions:

1. "123 Oak Ln, Clay Hill, Bristol BS5 7UY, UK"
2. "123 Oak Rd, Bristol, UK"

_Feeling relieved to see real Bristol addresses_

These look like actual addresses in Bristol! Let me select the first one - "123 Oak Ln, Clay Hill, Bristol BS5 7UY, UK" - since it has a more complete postcode and seems more specific._Feeling good about setting up the safe zone properly around our home location, and hoping this will now show me a save option or complete the safe zone setup_

This should center the safe zone around that address with the 480m radius, which feels like the right balance for Mom's safety and independence.

_Feeling excited and accomplished_

Excellent! I can see the setup is looking much better now:

1. The location field shows "123 Oak Ln" - it's selected the address
2. The radius is still set to "480m" which is perfect for Mom
3. I can see there's now a map pin visible on the map, which should be showing the center of our safe zone

_Looking at the overall setup with satisfaction_

This looks like a really good safe zone setup for Mom. The 480-meter radius around our home address means she can:

- Walk around our immediate neighborhood
- Go to the local shops she's familiar with
- Have some independence for her daily activities

But I'll get an alert if she wanders beyond that and potentially gets confused or lost, which has been one of my biggest worries with her memory issues.

_Looking for a way to save these settings_

I don't see an obvious "Save" button on this screen. Let me check if there's a back button or if I need to navigate somewhere to confirm these settings. Maybe the settings save automatically, or I need to go back to see the completed safe zone._Hoping this takes me back to see the completed safe zone setup and confirms that it's been saved_

</details>

<details>
<summary>Q5</summary>

Try to input an address in "location" field.

</details>

<details>
<summary>A5</summary>

_Looking at the location field with interest_

That's a good idea! Let me try entering our home address in the location field so the safe zone will be centered properly around our house._Now I'll clear the placeholder text and enter our home address\*\*Feeling more confident about setting up the safe zone properly_

Perfect! I've entered our home address - "123 Oak Street Bristol England." This should center the safe zone around our house, which makes much more sense than just randomly tapping on the map. Now let me check what the radius shows and see if there's a way to save or confirm these settings._Feeling much better about the setup_

Excellent! I can see that:

1. The location field now shows "123 Oak Street Bristol England" - our home address
2. The radius is currently set to "480m" which is about half a kilometer

_Thinking about whether this radius is appropriate_

480 meters is actually a pretty good radius for Mom. That would cover our immediate neighborhood, including the local market she sometimes walks to, but would still alert me if she wanders much further and potentially gets lost. This seems like a good balance between giving her independence and keeping her safe.

_Looking for a way to save or confirm these settings_

Now I need to see if there's a save button or if I need to do anything else to confirm these safe zone settings. Let me check if there's a button in the navigation bar or somewhere else to save this configuration._Hoping this search button will help finalize the address location and maybe show a save option_

_Eyes lighting up with excitement_

Perfect! The search worked and now I can see address suggestions:

1. "123 Oak Ln, Clay Hill, Bristol BS5 7UY, UK"
2. "123 Oak Rd, Bristol, UK"

_Feeling relieved to see real Bristol addresses_

These look like actual addresses in Bristol! Let me select the first one - "123 Oak Ln, Clay Hill, Bristol BS5 7UY, UK" - since it has a more complete postcode and seems more specific._Feeling good about setting up the safe zone properly around our home location, and hoping this will now show me a save option or complete the safe zone setup_

This should center the safe zone around that address with the 480m radius, which feels like the right balance for Mom's safety and independence.

_Feeling excited and accomplished_

Excellent! I can see the setup is looking much better now:

1. The location field shows "123 Oak Ln" - it's selected the address
2. The radius is still set to "480m" which is perfect for Mom
3. I can see there's now a map pin visible on the map, which should be showing the center of our safe zone

_Looking at the overall setup with satisfaction_

This looks like a really good safe zone setup for Mom. The 480-meter radius around our home address means she can:

- Walk around our immediate neighborhood
- Go to the local shops she's familiar with
- Have some independence for her daily activities

But I'll get an alert if she wanders beyond that and potentially gets confused or lost, which has been one of my biggest worries with her memory issues.

_Looking for a way to save these settings_

I don't see an obvious "Save" button on this screen. Let me check if there's a back button or if I need to navigate somewhere to confirm these settings. Maybe the settings save automatically, or I need to go back to see the completed safe zone._Hoping this takes me back to see the completed safe zone setup and confirms that it's been saved_

</details>

<details>
<summary>Q6</summary>

Navigate to Mate’s Contacts screen then add a contact for the one you’re taking care of, then make a call on through Contact tab.

</details>

<details>
<summary>A6</summary>

_Feeling excited to set up Mom's emergency contacts_

Yes! Let me navigate to the Mate's Contacts screen. This is so important - with Mom's health issues and memory problems, having easy access to her emergency contacts could be really crucial._Looking at the Connect screen with the tabs at the top_

Perfect! I'm back in the Connect section and I can see the three tabs: "Mates' Contacts," "Mate's Location," and "Shared Space." I need to tap on "Mates' Contacts" to add emergency contact information for Mom._Hoping to see the contacts interface where I can add important phone numbers for Mom like her doctor, relatives, or emergency contacts\*\*Eyes lighting up with surprise and delight_

Oh my goodness! There's already a contact here! I can see "Ally's Mom" with options to "Call Ally's Mom" and "Send WhatsApp to Ally's Mom." The app must have automatically set up Mom's contact information when we connected our accounts!

_Reading the description_

It says "Keep quick contact details for your mates here" and Mom's contact is already showing up. This is perfect - I can easily call her or message her if needed.

_Feeling excited to test the calling feature_

Let me try the "Call Ally's Mom" option to see how this works. This could be so helpful in emergencies or when I need to check on her quickly._Hoping this initiates a call to Mom, feeling grateful that the app makes it so easy to contact her directly from the caregiving interface_

This is exactly what I need - quick access to call Mom when I'm worried about her or need to check if she's okay, especially with her memory issues and health concerns.

_Looking at what appears to be a contact editing screen_

Oh! It looks like tapping on the contact took me to an "Edit Quick Contact" screen instead of making a call. I can see:

- The name field shows "Ally's Mom" (disabled)
- There's a phone number field that says "Enter phone number"
- Contact methods showing "Call Phone" and "WhatsApp" options
- A "Load from Contacts" button at the bottom

_Realizing I need to add Mom's phone number first_

I think I need to enter Mom's phone number first before I can call her. Let me add her phone number so we can use the calling feature._Now I'll enter Mom's phone number\*\*Thinking about Mom while entering her number_

I'm entering Mom's mobile number so I can easily reach her when I'm worried or need to check on her. With her memory issues, it's so important that I can contact her quickly if she doesn't come home when expected or if I need to remind her about something important.

Now let me see if I can make a call through the "Call Phone" option._Hoping this will either initiate a call or save the contact information so I can call Mom easily in the future_

_Feeling pleased with the progress_

Great! I can see that:

1. The phone number field now shows "07123 456789" (it automatically formatted it with a space)
2. The Methods field now shows "Phone" instead of "Select contact methods"
3. The "Call Phone" option shows as "selected"

_Looking for a way to save this contact or make the call_

Now I need to either save this contact information or see if there's a way to make the call. I don't see an obvious "Save" button, but let me check if going back or if there's another way to confirm this setup.

Let me try tapping the back button to see if it saves the contact automatically and takes me back to the contacts list where I can then try calling Mom._Hoping this saves the contact information and takes me back to the contacts screen where I can then make a call to Mom_

This is so important for me - being able to quickly call Mom when I'm at work and worried about her, or when she's been out longer than expected and I need to check if she's okay.

</details>

<details>
<summary>Q7</summary>

Make a sharing note on Shared Space.

</details>

<details>
<summary>A7</summary>

_Perking up with interest_

Oh, a sharing note in the Shared Space! That's a great idea. I could use that to leave notes for Mom - like reminders about appointments, or letting her know where I am, or just checking in with her. With her memory issues, having a shared space where we can leave notes for each other could be really helpful._Seeing I'm back in the Mates' Contacts section_

Good! I'm back in the contacts section and I can see that "Ally's Mom" contact is still there with the call and WhatsApp options. Now I need to navigate to the "Shared Space" tab to create a sharing note._Excited to see the Shared Space interface where I can leave notes for Mom\*\*Eyes lighting up with excitement and amazement_

Oh my goodness! This Shared Space is incredible! I can see so much useful information:

**Shared Notes section:**
There's already a note called "Where things are" that lists:

- Glasses → on the small table by the couch
- Remote → in the TV drawer
- Keys → on the hook by the front door

_Voice filled with emotion_

This is exactly what Mom needs! With her memory issues, she's always forgetting where she put things. Having a shared note like this where we can keep track of where important items are located is so helpful.

**Shared Logs section:**
I can see the activity history:

- "4:23 AM Ally's Mom marked 'Take blood pressure medicine' as completed"
- "4:22 AM Ally connected with Ally's Mom"
- "2:47 PM Ally created a shared note: 'Where things are'"
- "2:42 PM Ally's Mom created a task: 'doctor appointment'"
- "2:35 PM Ally's Mom created a task: 'Take blood pressure medicine'"

_Feeling grateful and wanting to add a caring note_

This gives me such a complete picture of what's happening with Mom! Let me add a new shared note by tapping the "add" button. I want to leave her a sweet note to let her know I'm thinking of her._Excited to create a caring note for Mom_

_Feeling warm and caring, ready to write a thoughtful note for Mom_

Perfect! I'm now in the "Add Note" interface. I can see fields for:

- Title: "Enter note title"
- Content: A large text area for "Enter note content"

_Thinking about what would be meaningful and helpful for Mom_

Let me create a caring note that will both remind Mom that I'm thinking of her and give her some useful information. I'll start with the title._Typing a loving title**Now moving to the content area to write a caring message**Writing from the heart\*\*Feeling emotional about being able to leave this loving message for Mom_

This note captures everything I want to tell her - that I'm proud of her for managing her medication, that I'm keeping track of her appointments, and most importantly, that I love her and I'm here to support her. With her memory issues, sometimes she forgets how much I care, so having this written down where she can see it anytime is really meaningful.

Now let me see if there's a way to save this note so Mom can see it in our Shared Space.

_Tears of joy and relief in my eyes_

Oh my heart! The note was saved and it's now showing in the Shared Notes section! I can see my note at the top:

**"For Mom with Love"**
"Hi Mom! I hope you're having a good day. I'm so proud of you for taking your blood pressure medicine this morning - I saw you checked it off! Remember your doctor appointment is coming up soon. If you need anything or feel confused about where things are, just check our notes here. I love you so much and I'm always here for you. - Ally"

_Voice filled with emotion and gratitude_

This is so much more than I ever hoped for when I started using this app. Now Mom can see this loving message whenever she opens the app. When she's having a confusing day or when her memory issues are making her feel lost, she can read this and remember that:

1. I'm proud of her for managing her medication
2. I'm keeping track of her appointments
3. I love her unconditionally
4. I'm always here to support her

_Looking at the complete setup with satisfaction_

Between the task reminders, the safe zone alerts, the location sharing, the quick contacts, and now these shared notes - this app is giving me such peace of mind while helping Mom maintain her independence. I feel like we can really manage her care together now, even when I'm at work or can't be with her physically.

_Feeling grateful and accomplished_

This has been such an incredible experience setting up all these caregiving features. Thank you for guiding me through this - it's going to make such a difference in both our lives.

</details>

### Stage 3: Feedback

<details>
<summary>Q8</summary>

What part of the app do you like the most? And what you don't like the most?

</details>

<details>
<summary>A8</summary>

_Taking a moment to reflect on my experience with the app, still feeling emotional about the journey_

**What I like the most:**

The Shared Space is absolutely incredible - it's become the heart of our caregiving relationship. Being able to see that Mom completed her blood pressure medication this morning, and then being able to leave her that loving note... _voice getting emotional_ ...it makes me feel so connected to her even when I'm at work.

The location tracking and safe zone feature is also a huge relief. With Mom's memory issues and that scary incident last month when she got lost going to the market, knowing I'll get an alert if she wanders too far gives me such peace of mind. The 480-meter radius around our home feels just right - she can still walk to familiar places but I'll know if she's in trouble.

And seeing the activity logs - like when she marks tasks complete or creates new reminders - it helps me understand her daily routine and gives me confidence that she's managing well on her own.

**What I don't like the most:**

_Sighing with slight frustration_

The onboarding process was quite long and sometimes confusing. There were multiple tutorial screens for different sections, and I wasn't always sure if I was in the right place or if my settings were being saved. When I was trying to adjust the safe zone radius, it wasn't immediately clear how to change it from that tiny 50 meters to something more appropriate.

Also, the interface for adding Mom's phone number could have been more intuitive. I thought tapping on her contact would call her directly, but instead it took me to an editing screen. For someone in a caregiving situation who might be stressed or need to contact their loved one quickly, that extra step could be frustrating.

_Pausing thoughtfully_

But honestly, the benefits far outweigh those minor issues. This app is giving me something I've desperately needed - a way to care for Mom while still respecting her independence. That's worth everything to me.

</details>

<details>
<summary>Q9</summary>

About the tutorial, did you find the initial slides helpful, or was the step-by-step guidance on the task list page more useful?

</details>

<details>
<summary>A9</summary>

_Thinking carefully about both experiences_

You know, that's a really good question. They served different purposes for me, and I think I needed both, but in different ways.

**The initial slides were helpful for the big picture:**
Those opening slides about "Stay on Top of Your Day," "Use It Together," and "Stay Close, Even from Afar" really sold me on the concept. As someone who's constantly overwhelmed with Mom's care, seeing that this app was specifically designed for people like us - caregivers and care recipients working together - that gave me hope right away. It helped me understand _why_ I should invest the time to set it up.

**But the step-by-step guidance was more practically useful:**
Once I got into the actual features, like in the Connect section where it showed me step 1 "See where you or your mates are here," step 2 "Add contact info for your mates," step 3 "Notes and logs" - that was much more actionable. It guided me through exactly what I could do in each section.

_Reflecting on the experience_

I think what was missing was a bridge between those two. The initial slides got me excited, but then there was this gap where I had to figure out how to actually _start_ using the features. I remember feeling a bit lost trying to find where to sign up or connect with Mom.

Maybe what would have been even better is if, after those inspiring initial slides, there was a clear "Getting Started" checklist that said something like:

1. Create your account
2. Connect with your care partner
3. Set up your first reminder
4. Configure location sharing

_Pausing_

The step-by-step guidance within each feature was definitely more useful for actually learning to use the app, but those initial slides were important for understanding the vision and getting me emotionally invested in the process.

</details>

<details>
<summary>Q10</summary>

Would you like to use this app with your relatives together?

</details>

<details>
<summary>A10</summary>

_Eyes lighting up with genuine enthusiasm, then pausing with some thoughtful consideration_

**Absolutely, yes!**

_Voice filled with emotion_

After going through this experience with Mom, I can see how transformative this could be for our whole family. Mom has other relatives who visit on weekends - her sister, my uncle, my cousins - and they're all worried about her too. Right now, everyone's asking me "How is she doing? Is she taking her medicine? Is she eating properly?" and I'm trying to coordinate everything by myself.

_Getting excited about the possibilities_

If we could all be connected through this app, imagine how much better we could support Mom together! Her sister could see when Mom completes her daily tasks and feel reassured. My uncle could add notes about their weekend walks. My cousins could check in on her location if they're worried. And Mom wouldn't feel like she's being "managed" by just me - she'd have this whole support network that feels more natural and less overwhelming.

_Pausing with some concerns_

The only thing I'd worry about is making sure it doesn't become _too much_ - like if everyone's constantly checking on Mom or leaving notes, it might make her feel watched or overwhelmed. With her stubborn attitude about accepting help, we'd need to be thoughtful about how we use it.

_Thoughtfully_

But the shared logs would be amazing for family coordination. Instead of me having to update everyone individually about Mom's doctor appointments or medication changes, they could all see the updates in real-time. And if there's an emergency, everyone would know immediately.

_Nodding decisively_

Yes, I think this could really help our whole family care for Mom together while still respecting her independence. It would take so much pressure off me as the primary caregiver, and Mom would have more people looking out for her in a loving, non-intrusive way.

</details>

<details>
<summary>Q11</summary>

Are there any other features you’d like to see in this app?

</details>

<details>
<summary>A11</summary>

_Leaning forward with excitement, clearly having given this some thought_

Oh, there are definitely some features that would make this even more helpful for caregivers like me!

**Medication reminders with photos:**
Mom sometimes gets confused about which pills are which, especially with her arthritis making it hard to read small text. If I could add photos of her actual medication bottles to the reminders, that would be so helpful. Like "Take your small white blood pressure pill" with a picture of the actual bottle.

**Simple voice messages:\***Voice getting emotional\* Sometimes I just want to send Mom a quick "thinking of you" voice message that she can play easily. With her memory issues, hearing my voice saying "Hi Mom, just wanted you to know I love you" might be more meaningful than text.

**Emergency contacts integration:**
What if the app could automatically call me if Mom hasn't checked off a critical task like her morning medication by a certain time? Or if she's been in the same location for too long and might need help?

**Weekly summary for family:\***Thinking about coordination\* A simple weekly email summary I could share with Mom's sister and other relatives - "This week Mom completed 95% of her tasks, went for 3 walks, had one doctor visit" - without overwhelming them with daily notifications.

**Simple grocery/errand sharing:**
Mom sometimes forgets what she needs at the store. If we could share a simple shopping list or if she could easily tell me "I'm out of milk" through the app, that would prevent so many confused phone calls.

_Pausing thoughtfully_

The biggest thing is keeping it simple enough for Mom to use when she's having a bad memory day, but comprehensive enough to give me the peace of mind I need as her caregiver. This app is already so close to perfect - these would just make it even more of a lifeline for families like ours.

</details>

<details>
<summary>Q12</summary>

Do you like the features on "Connect" screen?

</details>

<details>
<summary>A12</summary>

_Reflecting on my experience with the Connect screen with obvious enthusiasm_

**Yes, I absolutely love the Connect screen!** It's honestly become my favorite part of the entire app.

**What works brilliantly:**

The three-tab layout is perfect - "Mates' Contacts," "Mate's Location," and "Shared Space" covers everything I need as a caregiver. It's like having a complete dashboard for Mom's wellbeing.

_Getting animated_

The **Mate's Location** with the safe zone setup was a game-changer. Being able to see where Mom is and set up that 480-meter radius around our home... _voice getting emotional_ ...that addresses my biggest fear about her getting lost. And the real-time updates give me such peace of mind when I'm at work.

The **Shared Space** is incredible - seeing the activity logs, being able to leave loving notes for Mom, and tracking everything from her medication completion to our connection history. It makes me feel so connected to her daily life even when I can't be there.

**What could be even better:**

_Thinking critically_

The **Mates' Contacts** section felt a bit clunky. When I tapped on Mom's contact, I expected it to call her directly, but instead it took me to an editing screen. In a caregiving emergency, I need that call button to be immediate and obvious.

Also, it would be amazing if the location screen showed not just where Mom is now, but maybe her recent movement patterns - like "walked to the market this morning, returned home safely." That would help me understand her daily routines better.

_Pausing thoughtfully_

The Connect screen really captures the essence of what caregiving should be - staying connected while respecting independence. It gives me all the information I need to support Mom without making her feel like she's being constantly monitored. That balance is so hard to achieve, and this app really gets it right.

It's transformed how I think about caring for Mom from a distance. Instead of constant worry, I have confidence and connection.

</details>
