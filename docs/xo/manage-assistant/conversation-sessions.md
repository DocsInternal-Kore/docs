
# Conversation Sessions

	

		

			

Conversation sessions are defined as uninterrupted interactions between the bot and the user. These sessions are used in multiple analytics dashboards in the Bot Builder as well as Bot Admin Console platforms.

Kore.ai virtual assistant platform allows you to customize how these Conversation Sessions are to be created and closed.

!!! note

    Conversation Sessions are different from Billing Sessions,[ refer here](https://developer.kore.ai/docs/bots/bot-admin/billing/) for more on Billing Sessions.

		

	

	

		

			


## Overview

A Conversation Session is defined as an uninterrupted volley between the end user and the bot.



* Before the release of v7.2 of the platform – a new session was created after the _inactivity duration (set as 15 minutes)_ had elapsed since the end-user's last interaction.
* Post v7.2 release – after the _inactivity duration (set as 15 mins)_ has elapsed
    * if the end-user comes back and continues with the same intent, then the current session continues;
    * if the end-user comes back with a new intent or with an invalid input for the existing intent, a new session is created.
* Post v8.0 release, the platform gives you an option to:
    * Proactively close the sessions after inactivity – see[ Manage Sessions](https://developer.kore.ai/docs/bots/bot-settings/bot-sessions/#Manage_Sessions) to know more.
    * Not proactively close the sessions after inactivity – retain the v7.2 behavior described above;

Conversation Sessions are created for all interactions with the virtual assistant. These include:



* All conversations that include one or more messages from the user are marked as **interactive sessions**. These include all end-user interactions across all channels and events including providing authorization details.
* All Virtual assistant-initiated conversion sessions like onConnect event messages are recorded as **non-interactive**. These sessions will be updated as Interactive sessions as soon as a user message is received. Non-interactive sessions are not considered for calculating the billing sessions.
* **Developer interactions** are also included as conversation sessions. A flag differentiates the user sessions from developer sessions and billing sessions are not created for these developer sessions.

!!! note

     The inclusion of non-interactive and developer interactions in conversation sessions was implemented starting from ver8.0.

		

	

	

		

			


## Manage Sessions

This feature is only available post v8.0 of the platform release.

You can define the Conversation Session behavior using the **Manage Sessions** option under **Configurations** from the **Build** tab.



![alt_text](images/conversationsessions1.png "image_tooltip")


The following details explain the options available on the page, to define the conversation sessions.



* **Do not proactively close the sessions after inactivity** – Select this option to close the session only when the user returns after 15 minutes of inactivity and provides a new intent. This was the default behavior before the release of ver8.0 of the platform. <span style="text-decoration:underline;">This option will be deprecated in future releases</span>.
* **Proactively close the sessions after inactivity** – Select this option to close the session after a defined duration of inactivity. You can set the following parameters:
    * **Inactivity Duration** – this is set to 15 minutes by default. The session closes after the time duration set here.
    
    !!! note

        The minimum value that can be set here is **5 min ** and the maximum value is **20160** **min** (14 days). These values can be configured at the application level through Koreconfig.

* **Session Closure Behavior** – You can choose to close the session without informing the user or inform the user about the session closure by sending out a message. This message can be customized using the **Manage Response** link. You can click **Add Response** if you want to add a new response. 



    ![alt_text](images/conversationsessions2.png "image_tooltip")

* **Clear Auth Profile** – You can enable the **Clear Auth Profiles** option to clear all authorization tokens and session variables associated with a particular session. Once you enable this setting, you are required to provide the authorization profile details again to re-authorize the session. 



![alt_text](images/conversationsessions3.png "image_tooltip")

* **Run Custom Script** – You can use the custom script to invoke koreUtil.ClearAuthProfiles function to clear the authorization profile and associated session variables for that particular profile. For example, if you have enabled multiple authorization profiles for a session, you can use the `koreUtil.ClearAuthProfiles` to disable a particular authorization profile that is not needed for this session using this custom script: 
 `koreUtil.ClearAuthProfiles ( [Auth_Profile_Name] )` 
You can also clear all authorization profiles using this script: 
`koreUtil.ClearAllAuthProfiles ( )` For more information, see[ kore.UtilLibraries](https://developer.kore.ai/docs/bots/advanced-topics/koreutil-libraries/)<span style="text-decoration:underline;"> </span>article.



    ![alt_text](images/conversationsessions4.png "image_tooltip")


		

	

	

		

			


## Implementation

**When does a Conversation Session start?**

Conversation Sessions are created for all interactions:



* All **end-user interactions** across all channels and events – Conversation sessions are created for On_connect – Run a script, Run a Message, Trigger a Dialog scenario. There are two categories of these conversation sessions:
    * **Interactive sessions** are conversations that include one or more messages from the user.
    * **Non-interactive sessions** are conversations with no messages from the user. All bot-initiated conversion sessions start as ‘Non-interactive’. These sessions are updated as Interactive sessions as soon as a user message is received. The non-interactive sessions are not considered for calculating the billing sessions.
* **Developer interactions** will also be considered for creating conversation sessions but these are marked as different from the user sessions and are not considered for Billing Sessions.

**When does a Conversation Session close?**



* The platform proactively closes inactive sessions after the specified time of inactivity set in the[ Manage Sessions](https://developer.kore.ai/docs/bots/bot-settings/bot-sessions/#Manage_Sessions)<span style="text-decoration:underline;"></span> option.
* When the following utterances are detected – _“Discard”_
* When the chat window is refreshed, "_refresh: true” _is detected.

		

	

	

		

			

**What happens when a Conversation Session closes?**



* Post-session closure, the following information or variables will be cleared:
    * Conversation session;
    * Bot User Session (developer-defined variables without custom TTL)
    * Dialog Context (Topic File and Conversation Details)
    * If configured, before closing the conversation session, the platform will proactively send a session closure message to the users on supported channels.
* For “_refresh: true_”:
    * Complete session information is cleared;
    * A new conversation session is created.
* For “_discard all_”
    * The Dialog context, Current and Historic Tags are cleared;
    * The Sentiment Tones are reset;
    * The same Conversation Session will be continued
* For “_discard_”
    * The current Dialog context will be cleared;
    * The Current Tags will be replaced with the last updated ‘tags’ in the Historic Tags, and the Historic Tags will be cleared;

		
