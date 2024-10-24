# NICE MAX Desktop Chat and Voice

This document provides detailed instructions on the integration process of the Kore.ai Agent AI widget into the NICE MAX Desktop environment. It offers step-by-step guidance to ensure a smooth and efficient setup process, covering all necessary aspects of integration from start to finish. This integration will support all outstanding features of Agent AI such as [Automation](https://docs.kore.ai/agentassist/onboarding/conversation-automation/){:target="_blank"}, [Agent Coaching](https://docs.kore.ai/agentassist/agent/agent-coaching/){:target="_blank"}, [Agent Playbook](https://docs.kore.ai/agentassist/agent/agentassist-playbook/){:target="_blank"}, [Sentiment Analysis](https://docs.kore.ai/agentassist/agent/agentassist-widget/){:target="_blank"}, [Transcription](https://docs.kore.ai/agentassist/agent/agentassist-widget/#Transcript_Tab){:target="_blank"} along with end of call summary and Custom Data passing such as agent name, ID etc to Agent AI widget.

## **Shared Responsibilities**

### **NICE CXOne Admin**

* **ACD Configuration:** CXOne customers are responsible for creating and mapping skills within the ACD system to ensure proper routing of interactions.
* **Campaign Setup:** Customers must set up campaigns, including specifying routing and agent availability, on the CXOne platform.
* **Signal API Access:** Customers must configure NICE CXOne authentication to allow Kore.ai bots to interact with CXOne’s Signal API.
* **Agent Assist Hub Configuration:** CXOne customers are responsible for configuring the Agent Assist Hub settings within NICE Studio.

### **Kore.ai Admin**

* **Provide Studio Script for Chat and Voice:** Kore.ai will assist in provisioning the Studio script to ensure seamless integration with the CXOne platform.

## **Prerequisites**

* NiceCX administrator having access to a NICE CX Account and with privileges to set up the below configurations and able to receive calls and chats on agent desktop.
* [NICE CX Studio](https://help.nice-incontact.com/content/studio/studio.htm){:target="_blank"} installed on your windows device.
* Agent Assist Hub enabled for your account. Contact your NICE CX representative. Note this requires an extra license cost.
* Access to Kore AgentAssist application and familiarity with creating and configuring an AgentAssist Bot.
* Kore.ai App credentials such as Agent AI Widget URL, Bot ID, Client ID, Client Secret, Account ID and SIP URI. Read [Configure Voice Channel](https://docs.kore.ai/agentassist/channels/voice/){:target="_blank"} and [Chat](https://docs.kore.ai/agentassist/channels/chat/){:target="_blank"} for a walkthrough.

## **Definitions**

<table>
  <tr>
   <td><strong>Section</strong>
   </td>
   <td><strong>Key</strong>
   </td>
   <td><strong>Definition</strong>
   </td>
   <td><strong>Reference</strong>
   </td>
  </tr>
  <tr>
   <td>Nice CX Integration Hubs > Add Agent Assist App
   </td>
   <td>Agent AI URL
   </td>
   <td><p><span id="adn">The domain of the Agent AI.</span></p>
   </td>
   <td>
<ul>

<li>If it is legacy Agent AI, URL is <a href="https://agentassist.kore.ai" target=" blank">https://agentassist.kore.ai</a></li>

<li>If it is UXO, URL is <a href="https://platform.kore.ai" target=" blank">https://platform.kore.ai</a></li>

<li>If it is on-prem, the URL is the origin where your Agent AI is hosted.</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>NICE CX Studio > Import Chat & Voice Scripts and Configure Parameters
   </td>
   <td>AgentAssistWidgetURL
   </td>
   <td>URL that points to the Agent AI widget.
<p>
For example, https://agentassist.kore.ai/koreagentassist-sdk-v3/UI/agentassist-iframe.html
   </td>
   <td><strong>Channels > Chat</strong> section of the <a href="https://agentassist.kore.ai" target=" blank">Agent AI</a> configuration portal.
   </td>
  </tr>
  <tr>
   <td>Nice CX Integration Hubs > Add Agent Assist App
<p>
+
<p>
NICE CX Studio > Import Chat & Voice Scripts and Configure Parameters
   </td>
   <td>BotId
   </td>
   <td>A unique identifier assigned to a bot.
   </td>
   <td><strong>Channels > Chat</strong> section of the <a href="https://agentassist.kore.ai" target=" blank">Agent AI</a> configuration portal.
   </td>
  </tr>
  <tr>
   <td>Nice CX Integration Hubs > Add Agent Assist App
<p>
+
<p>
NICE CX Studio > Import Chat & Voice Scripts and Configure Parameters
   </td>
   <td>ClientId
   </td>
   <td>An identifier provided to a client application.
   </td>
   <td><strong>Channels > Chat</strong> section of the <a href="https://agentassist.kore.ai" target="_blank">Agent AI</a> configuration portal.
   </td>
  </tr>
  <tr>
   <td>Nice CX Integration Hubs > Add Agent Assist App
<p>
+
<p>
NICE CX Studio > Import Chat & Voice Scripts and Configure Parameters
   </td>
   <td>ClientSecret
   </td>
   <td>A secret key or password associated with the ClientId.
   </td>
   <td><strong>Channels > Chat</strong> section of the <a href="https://agentassist.kore.ai" target="_blank">Agent AI</a> configuration portal.
   </td>
  </tr>
  <tr>
   <td>Nice CX Integration Hubs > Add Agent Assist App
   </td>
   <td>AccountID
   </td>
   <td>A unique identifier assigned to an account.
   </td>
   <td><strong>Channels > Chat</strong> section of the <a href="https://agentassist.kore.ai" target=" blank">Agent AI</a> configuration portal.
   </td>
  </tr>
  <tr>
   <td>Nice CX Integration Hubs > Add Agent Assist App
   </td>
   <td>Kore Voice Gateway(KVG)
   </td>
   <td><p><span id="kvg">For Saas in US region, value is wss://savg-webserver.kore.ai</span></p>
<p>
For on-prem, refer to corresponding host<strong> </strong>
   </td>
   <td>
   </td>
  </tr>
</table>

**Region Specific URLs**

<table>
  <tr>
   <td><strong>Region</strong>
   </td>
   <td><strong>Agent AI URL</strong>
   </td>
   <td><strong>WSS URL</strong>
   </td>
   <td><strong>DNS</strong>
   </td>
  </tr>
  <tr>
   <td>US
   </td>
   <td><a href="https://agentassist.kore.ai" target=" blank">https://agentassist.kore.ai</a>
   </td>
   <td>wss://savg-webserver.kore.ai
   </td>
   <td>@savg-us-prod-sbc-in-nlb-0d9a4c651955ff47.elb.us-east-1.amazonaws.com
   </td>
  </tr>
  <tr>
   <td>JP
   </td>
   <td><a href="https://agentassist-jp.kore.ai" target=" blank">https://agentassist-jp.kore.ai</a>
   </td>
   <td>wss://jp-savg-audiosocket.kore.ai
   </td>
   <td>@savg-jp-prod-int-nlb-3989d946fc1ced3b.elb.ap-northeast-1.amazonaws.com
   </td>
  </tr>
</table>

## Configuration Steps

This section explains the configuration steps needed to integrate Kore Agent AI with NICE MAX Desktop.

* [NICE CX Integration Hubs, Add Agent Assist Hub](#nice-cx-integration-hubs-add-agent-assist-hub)
* [NICE CX Studio, Import Chat and Voice Scripts and Configure Parameters](#nice-cx-studio-import-chat-voice-scripts-and-configure-parameters)
* [NICE CX Setup, Attach Point of Contact with Chat/Voice Script](#nice-cx-setup-attach-point-of-contact-with-chatvoice-script)
* [Access Data in Agent AI Bot](#access-custom-data-in-agent-ai-bot)
* [Chat Simulation](#chat-simulation)
* [Voice Simulation](#voice-simulation)

## **Nice CX Integration Hubs > Add Agent Assist Hub**

1. Sign in to your **NICE** account with the user name and password provided by the NICE customer support.
2. Click the **Applications Launcher** button.  
<img src="../nice-max-images/application-launcher-button-1.png" alt="application-launcher-button" title="application-launcher-button" style="border: 1px solid gray; zoom:80%;">

3. A menu opens from the left side of the page. Click **OTHERS** > **Automation & AI**.  
<img src="../nice-max-images/automation-ai-2.png" alt="automation-ai" title="automation-ai" style="border: 1px solid gray; zoom:80%;">

4. Click **Agent Assist Hub** > **Add Agent Assist App**.  
<img src="../nice-max-images/add-agent-assist-app-3.png" alt="add-agent-assist-app" title="add-agent-assist-app" style="border: 1px solid gray; zoom:80%;">

1. Enter the name of the **Agent Assist App** in the **AGENT ASSIST APP NAME** field.
2. Select **Custom Agent Assist Endpoints**.
3. Click **Next**.  
<img src="../nice-max-images/custom-agent-assist-endpoint-4.png" alt="custom-agent-assist-endpoint" title="custom-agent-assist-endpoint" style="border: 1px solid gray; zoom:80%;">

4. Add the following settings with config parameters:
    1. Agent UI Option: Available by default 
    2. App URL: {<a href="#adn">Agent AI URL</a>}/integrations/nice/iframe/?params={scriptparams}
    3. App Title: Kore Agent AI (change as needed)
    4. Participants: Both
    5. Text Relay Endpoint:{<a href="#adn">Agent AI URL</a>}/integrations/nice/relay/toKore  
    <img src="../nice-max-images/configuration-5.png" alt="configuration" title="configuration" style="border: 1px solid gray; zoom:80%;">

    6. Audio Relay Endpoint: {<a href="#kvg">Kore Voice Gateway(KVG)</a>}/audiosocket/nice?sipuri=&lt;Bot SIP URI>&lt;DNS>&token=&lt;Token>&botId=&lt;Bot ID>&accountId=&lt;Account ID>&agentassist=true
        * Bot SIP URI : **Channels > Voice** section of the **[Agent AI](https://agentassist.kore.ai){:target="_blank"}** configuration portal.  
        <img src="../nice-max-images/sip-id-6.png" alt="sip-id" title="sip-id" style="border: 1px solid gray; zoom:80%;">

        * Bot ID and Account ID: **Channels** > **Chat** section of the **[Agent AI](https://agentassist.kore.ai){:target="_blank"}** configuration portal.  
        <img src="../nice-max-images/chat-section-7.png" alt="chat-section" title="chat-section" style="border: 1px solid gray; zoom:80%;">

        * Token: Create a **JSON Web Token** on jwt.io with the following details:
            * Payload: {“appId”: &lt;Bot Client ID>}
            * Header: {“alg”: “HS256″,”typ”: “JWT”}
            * Secret: Bot Client Secret.
1. Scroll down and add the following Configuration Parameters. (only for chat)  
<img src="../nice-max-images/configuration-parameters-8.png" alt="configuration-parameters" title="configuration-parameters" style="border: 1px solid gray; zoom:80%;">

2. Click **Create**.

## **NICE CX Studio > Import Chat & Voice Scripts and Configure Parameters**

1. Download the [script for chat](https://bitbucket.org/koreteam1/integration_sharedresources/src/main/nicecx/kore.ai%20-%20nice_agentassistchat.xml){:target="_blank"} / [script for voice](https://bitbucket.org/koreteam1/integration_sharedresources/src/main/nicecx/kore.ai%20-%20nice_agentassistvoice.xml){:target="_blank"} from the **Kore.ai Nice integration** repository.
2. Open the **NICE CX Studio** app from your desktop.
3. Click **File** > **Import from File**.
4. Select the **downloaded script** for chat / voice.
5. Double-click the **Generate Iframe Params** tile.  
<img src="../nice-max-images/generate-iframe-param-9.png" alt="generate-iframe-param" title="generate-iframe-param" style="border: 1px solid gray; zoom:80%;">  

    <img src="../nice-max-images/generate-iframe-param2-10.png" alt="generate-iframe-param" title="generate-iframe-param" style="border: 1px solid gray; zoom:80%;">

6. Update the values for the corresponding parameters:
    1. Kore.ai Parameters
        1. Bot Client ID
        2. Bot Client Secret
        3. Bot ID
        4. Agent AI Widget URL
    2. Custom Data: The “customdata” object in the script can be used to pass information to the Agent AI Bot. During runtime, this customdata will be accessible in the UserContext of the bot. Refer to [Access Custom Data in Agent AI Bot](#access-custom-data-in-agent-ai-bot) for instructions on how to access customdata in the bot. 
 
        Include your data in the customdata object (one key-value pair per line). For example: 

            1. `customdata.agentName="Agent"`

            2. `customdata.agentID="1234"`

    3. NICE CX Credentials: Base region URL is the Host URL of the login page. If the URL for ACD is **https://home-abc.nice-incontact.com**, then the API URL would be **https://api-abc.nice-incontact.com**. Also, it is necessary to use the URLs without the trailing slash.
        1. NICE CX API Access Key
        2. NICE CX API Access Key Secret
        3. NICE CX API URL
        4. NICE CX Base Region URL
        !!! note
            Refer to [https://help.nice-incontact.com/content/admin/security/manageaccesskeys.htm](https://help.nice-incontact.com/content/admin/security/manageaccesskeys.htm){:target="_blank"} to create NICE CX API Access Key and NICE CX API Access Key Secret. 

7. Double-click the **Agent Assist** tile.  
<img src="../nice-max-images/agent-assist-tile-11.png" alt="agent-assist-tile" title="agent-assist-tile" style="border: 1px solid gray; zoom:80%;">

8. Select the **checkbox** against the Agent Assist instance you created in the above step.  
<img src="../nice-max-images/agent-assist-instance-12.png" alt="agent-assist-instance" title="agent-assist-instance" style="border: 1px solid gray; zoom:80%;">

9. Click **Yes**.  
<img src="../nice-max-images/studio-action-13.png" alt="studio-action" title="studio-action" style="border: 1px solid gray; zoom:80%;">

10. After selecting **Agent Assist**, click the **Close** button on the bottom-right corner of the page. 
!!! note
    Do not click the “X” button to close the window as this will not save the changes. 

## **NICE CX Setup > Attach Point of Contact with Chat/Voice Script**

1. Go to the **NICE** home page.
2. Click the **Application Launcher** button.
3. Click **ACD**.
4. Click **Points of Contact**.
5. Click the **Chat Endpoint** you want to attach with AgentAssist. For voice, click the **number** you want to attach with AgentAssist.
6. Click **Edit**.
7. Change the **script** based on your needs.
8. Click **Done** to save it.

## Access Custom Data in Agent AI Bot

You can access Custom Data in **Welcome Events** in **Agent AI configuration** page and in **Dialog Tasks** in **Agent AI automation** page.

Custom Data can be accessed as

```
{{context.session.UserContext.customData.<key>}}
```

**Welcome Events:**  
<img src="../nice-max-images/welcome-events-14.png" alt="free text" title="free text" style="border: 1px solid gray; zoom:80%;">

**Dialog Tasks:**

In the **Dialog Task**, open a **Message** node, and click **MANAGE RESPONSES**.  
<img src="../nice-max-images/manage-responses-15.png" alt="manage-responses" title="manage-responses" style="border: 1px solid gray; zoom:80%;">  

<img src="../nice-max-images/plain-responses-16.png" alt="plain-responses" title="plain-responses" style="border: 1px solid gray; zoom:80%;">

<img src="../nice-max-images/java-script-response-17.png" alt="java-script-response" title="java-script-response" style="border: 1px solid gray; zoom:80%;">

## Chat Simulation

1. Go to the **NICE** home page.
2. Click the **Application Launcher** button.
3. Click **MAX**.  
<img src="../nice-max-images/chat-simulation-18.png" alt="chat-simulation" title="chat-simulation" style="border: 1px solid gray; zoom:80%;">

4. Select **Integrated Softphone,** and click **Connect**.
5. Change the status to **Available**.  
<img src="../nice-max-images/chat-available-19.png" alt="chat-available" title="chat-available" style="border: 1px solid gray; zoom:80%;">  

6. Go back to the **NICE** home page, and click **Application Launcher** > **ACD**.
7. Click **Points of Contact**.
8. Click the Chat **Point of Contact** you have created.  
<img src="../nice-max-images/chat-point-of-contact-20.png" alt="chat-point-of-contact" title="chat-point-of-contact" style="border: 1px solid gray; zoom:80%;">
    
9. Copy the **Point of Contact URL**, and open it in a new tab.
10. Initiate the chat from here. A chat request appears on the **MAX** desktop.
11. Click **Accept**.  
<img src="../nice-max-images/accept-chat-request-21.png" alt="accept-chat-request" title="accept-chat-request" style="border: 1px solid gray; zoom:80%;">  

    <img src="../nice-max-images/chat-simulation-realtime-22.png" alt="chat-simulation-realtime" title="chat-simulation-realtime" style="border: 1px solid gray; zoom:80%;">

## Voice Simulation

1. Go to the **NICE** home page.
2. Click **Application Launcher** > **MAX**.  
<img src="../nice-max-images/voice-simulation-23.png" alt="voice-simulation" title="voice-simulation" style="border: 1px solid gray; zoom:80%;">

3. Select **Integrated Softphone**, and click **Connect**.
4. Change the status to **Available**.  
<img src="../nice-max-images/voice-available-24.png" alt="voice-available" title="voice-available" style="border: 1px solid gray; zoom:80%;">

5. Go back to the **NICE** home page, and click **Application Launcher** > **ACD**.
6. Click **Points of Contact**.
7. Click the Voice **Point of Contact** you have created.  
<img src="../nice-max-images/voice-point-of-contact-25.png" alt="voice-point-of-contact" title="voice-point-of-contact" style="border: 1px solid gray; zoom:80%;">

8. Copy the **Phone Number,** and initiate the call.
9. A voice request appears on the **MAX** desktop. Click **Accept**.  
<img src="../nice-max-images/accept-voice-26.png" alt="accept-voice" title="accept-voice" style="border: 1px solid gray; zoom:80%;">

    <img src="../nice-max-images/voice-realtime-27.png" alt="voice-realtime" title="voice-realtime" style="border: 1px solid gray; zoom:80%;">