---
description: This will show your requirements to start using the JSON and Folder Handlers
---

# Basic Setup

Sadly, pqko-discord setups up your full environment meaning pqko-discord handles the discord.js client.

```javascript
const { client_id, client_secret, token } = require("./config.json")

const { Client, GatewayIntentBits } = require("discord.js")
const client = new Client({ intents: [GatewayIntentBits.Guilds] }); // The intents might not be correct...

const PqkoDiscord = require("pqko-discord") // Calls main package
const pqko = new PqkoDiscord.SlashCommands(token, client_id, client_secret, client)

pqko.login() //or client.login(token)
```

