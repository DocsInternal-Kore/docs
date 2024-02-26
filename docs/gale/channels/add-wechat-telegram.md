# Adding the WeChat Channel

To set up WeChat as a channel, you need to register for a WeChat Official Account. You also need to enable webhook integrations for the XO Platform to send and receive messages.

Please refer to the WeChat Official Accounts [Registration Process](https://admin.wechat.com/cgi-bin/readtemplate?t=ibg_en/en_faq_tmpl&type=info&lang=en_US) for more information.

For development purposes, you may also use the WeChat Sandbox environment to integrate the assistant and test functionality. This article takes you through the setup process.


## Step 1: Set up a WeChat Sandbox Account


1. Register and login to the WeChat Sandbox environment from [here for English](https://mp.weixin.qq.com/?lang=en_US&token=) and [here for Chinese](https://mp.weixin.qq.com/?lang=zh_CN&token=) versions.
2. Click the **Login** button to continue.
3. You would be required to install the WeChat mobile app to allow sign in using the QR presented on-screen.
4. Scan the **QR code** and confirm Login to proceed.
5. Post successful sign-in, you would be redirected to the Sandbox portal.
6. The Sandbox portal provides information about your WeChat Sandbox App ID and App Secret.
7. Make note of **App ID** and **App Secret**.
8. You need to enter the WebHook **URL** and **Token**, you can obtain these values from the Channel page of the XO Platform as explained below.


## Step 2: Set up a Webhook


1. In the XO Platform, select the assistant that you want to add the WeChat channel to.
2. Go to **Deploy > Channels**, and select **WeChat**.
3. Navigate to the **Configurations** tab and enter the following details:
    * **App Id** – _App Id _from the weChat Sandbox portal page
    * **App Password** – _App Secret_ from the weChat Sandbox portal page
4. Make a note the following details
    * _Webhook URL_, and
    * _Access Token_
5. Update the **WeChat Sandbox portal page** with the above URL and access token and **Save** the details
6. **Enable** the weChat channel from the XO Platform.
<img src="../images/wechat.png" alt="wechat channel configuration" title="wechat channel configuration" style="border: 1px solid gray; zoom:70%;">


After the channel is enabled and all configurations are verified, you can optionally publish the assistant to make it available for end-users, with the new channel. Learn more about[ Publishing your Virtual Assistant](https://developer.kore.ai/docs/bots/publish/publishing-bot/).

To learn more about working with Channels within the Kore.ai XO Platform, please see[ Channel Enablement.](https://developer.kore.ai/docs/bots/channel-enablement/adding-channels-to-your-bot/)
