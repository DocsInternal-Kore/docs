<!-----

You have some errors, warnings, or alerts. If you are using reckless mode, turn it off to see inline alerts.
* ERRORs: 0
* WARNINGs: 0
* ALERTS: 11

Conversion time: 3.896 seconds.


Using this Markdown file:

1. Paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β34
* Fri Nov 10 2023 02:01:32 GMT-0800 (PST)
* Source doc: Languages and Speech
* This document has images: check for >>>>>  gd2md-html alert:  inline image link in generated source and store images to your server. NOTE: Images in exported zip file from Google Docs may not appear in  the same order as they do in your doc. Please check the images!

----->

# **Languages and Speech**

This feature lets you configure the language and speech settings within Contact Center module, to manage how your contact center uses languages and speech recognition.

Go to **Contact Center > CONFIGURATIONS > Languages & Speech** to access Languages and Speech settings.
<img src="../images/languages-and-speech-page.png" alt="
Languages & Speech Page" title="Languages & Speech Page" style="border: 1px solid gray; zoom:80%;">

This section of the Contact Center module provides access to the following settings:

* **[Supported languages](https://docs.kore.ai/smartassist/settings/general-settings/language-management/#)**: Define the languages you want agents and automation to work with.
* **[Voice Preferences](https://docs.kore.ai/smartassist/settings/advanced-settings/)**: Choose the engines to use with SmartAssist for Automated Speech Recognition (ASR) and Text-to-Speech (TTS).
* **[Hold Audio](https://docs.kore.ai/smartassist/agent/default-agent-interaction-flows/#Hold_Audio)**: Define the default audio that plays to callers while on hold or waiting in the queue.

## Language Management

This feature helps manage the languages that are supported by the contact center infrastructure. You can add support for specific languages and enable, disable or delete specific languages.

To manage languages, click **Supported Languages**.
<img src="../images/supported-languages.png" alt="
Supported Languages Panel" title="Supported Languages Panel" style="border: 1px solid gray; zoom:80%;">

### Add a Language

To add a new language, follow these steps:

1. In the **Language** panel, select the language and click on **Agent, Call Automation, Chat Automation** or _select all_ to enable the language for each functionality.
2. Click **Save** to save your new language.
<img src="../images/add-language-window.png" alt="
Add Language Window" title="Add Language Window" style="border: 1px solid gray; zoom:80%;">

### Disable and Re-Enable a Language

To disable a language and its access flows, uncheck its corresponding checkbox, then click **Save**. This will deactivate the language, and it will no longer be available within the selected access channels; however, it will not be completely removed.

You can enable the language again later by selecting its corresponding checkbox, then saving.
<img src="../images/language-checkbox.png" alt="
Enable Language Check-box" title="Enable Language Check-box" style="border: 1px solid gray; zoom:80%;">

### Delete a Language

In the **Language** panel, click the **Delete (bin)** icon for the language you want to remove. This removes the language completely from all your workflows.
<img src="../images/delete-language.png" alt="
Delete Language" title="Delete Language" style="border: 1px solid gray; zoom:80%;">

## Voice Preferences

In the Language & Speech section of SmartAssist, you can configure the voice preferences to personalize the ASR Engine and the voice that plays for your text-to-speech conversions.

To configure or modify the voice preferences, follow the steps below:

1. Under **Languages & Speech**, click **Voice Preferences**.
<img src="../images/voice-preferences.png" alt="
Voice Preferences" title="Voice Preferences" style="border: 1px solid gray; zoom:80%;">

2. Select a **Text-to-Speech Engine** in the _Voice Preferences_ window: _Google Cloud Text-to-Speech, Microsoft Azure Speech Services,_ or _AWS Amazon Polly._
    1. Enter **Sample Text** to preview your voice selection. You can play, navigate through the audio (Back/Fw), and adjust the preview volume. Clicking the More Options (⋮) button reveals options to adjust **Playback Speed** and **Download** the voice preview.
    2. Click the **Play** button next to any available voice to preview it. Voices are available for all TTS engines, but each engine has its own voice options.
    3. Select a different Voice Language if required.
    <img src="../images/configure-voice-preferences.gif" alt="Configure Voice Preferences" title="Configure Voice Preferences" style="border: 1px solid gray; zoom:80%;">

3. Select an **Automated Speech Recognition Engine**: Google Cloud Speech-to-Text, Microsoft Azure Speech Services, AmiVoice, or NVIDIA Riva. Afterward, choose the **Dialect** that you want to work with.
<img src="../images/asr-and-dialect.png" alt="
Select ASR and Dialect" title="Select ASR and Dialect" style="border: 1px solid gray; zoom:80%;">

4. Click **Done** once you have completed configuring your voice preferences. The set voice, language, and dialect apply to automated customer responses that use text-to-speech.

## Hold Audio

This option helps configure the audio played to a caller while on hold or waiting in the queue.

To configure the **Hold Audio**, go to **Languages & Speech** and select the **Hold Audio** option.
<img src="../images/hold-audio.png" alt="
Hold Audio" title="Hold Audio" style="border: 1px solid gray; zoom:80%;">

### Add Hold Audio Files

1. In the **Hold Audio** panel, click **Browse** to select and upload your _.WAV_ audio file. Alternatively, you can drag and drop the file to the panel.
1. Once the file uploads, you can adjust the audio file name in the **Rename Audio** text area.
2. Click **Save** to add the new audio file and it is automatically added to the **Hold Audio** list. The uploaded audio plays to the caller while on hold or waiting in the queue.
<img src="../images/configure-hold-tone.gif" alt="
Add Hold Audio" title="Add Hold Audio" style="border: 1px solid gray; zoom:80%;">

### Delete Hold Audio Files

The available audio file deletion methods are listed below and illustrated in the following screenshot:

1. Delete a file from the saved list by clicking the **Delete (bin)** icon next to it. You will be asked to confirm your choice. Files deleted from the list have to be reuploaded if you change your mind.
2. Remove an uploaded file that has not yet been saved to the list by clicking the **Delete (x)** button on the top right corner of the upload panel.
<img src="../images/delete-audio-file.png" alt="
Delete Audio File" title="Delete Audio File" style="border: 1px solid gray; zoom:80%;">