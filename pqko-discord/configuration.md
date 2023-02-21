---
description: Pqko-Discord required config
---

# Configuration

Like any other package we require config for the handler(s) to use! This guide will show step by step what to do

If you need any help watch the video: Coming Soon

Go the [discord developer portal](https://discord.com/developers/applications) and press the "New Application" Button or go on ur existing application

<figure><img src="../.gitbook/assets/Create Application.png" alt=""><figcaption></figcaption></figure>

Next put your application's name in our case "Pqko-Disxord" , after that agree to Discord's TOS and Developer Policy, and then press "Create". Like the image shows bellow!

<figure><img src="../.gitbook/assets/Name, Policy, Create.png" alt=""><figcaption></figcaption></figure>

Then create a config file something like this.

```json
{
  "client_id": "",
  "client_secret": "",
  "token": ""
}
```

Now back on the developer portal and on the application head over to the "OAuth2" Page

<figure><img src="../.gitbook/assets/Application to OAuth2 Page.png" alt=""><figcaption></figcaption></figure>

Now copy the "Client ID" and insert it into the JSON File containing our Client ID, Secret and Token

<figure><img src="../.gitbook/assets/Copy Client ID.png" alt=""><figcaption></figcaption></figure>

Now reset the "Client Secret" and copy it and insert it to the JSON File

<figure><img src="../.gitbook/assets/Reset and Copy Client Secret.png" alt=""><figcaption></figcaption></figure>

Now head over the the "Bot" Page on the sidebar.

<figure><img src="../.gitbook/assets/OAuth2 To Bot.png" alt=""><figcaption></figcaption></figure>

Now press the "Add Bot".

<figure><img src="../.gitbook/assets/Add Bot.png" alt=""><figcaption></figcaption></figure>

If this is a private bot you might wanna tick off the "PUBLIC BOT" Option

<figure><img src="../.gitbook/assets/Public Bot option.png" alt=""><figcaption></figcaption></figure>

Now press on the "Reset Token" Button or "View Button" then press "Copy" and paste it in your config file (JSON)

<figure><img src="../.gitbook/assets/Reset Token and Copy.png" alt=""><figcaption></figcaption></figure>

Optional: If you are going to use Slash Commands you require these 2 intents enabled on the bots page

<figure><img src="../.gitbook/assets/REQUIRED INTENTS.png" alt=""><figcaption></figcaption></figure>

Optional: Scroll down on the page and enable "SERVER MEMBERS INTENT". This is required for the OAuth2 Join Function!

<figure><img src="../.gitbook/assets/Server Members Intent.png" alt=""><figcaption></figcaption></figure>
