---
description: The required setup
---

# Basic Setup

Its actually suprisngly small for what its actually meant for the event handler to work

```javascript
const { client_id, client_secret, token } = require("./config.json")

const { Client } = require("discord.js")
const client = new Client({ intents: [] }); // The intents might not be correct...

const PqkoDiscord = require("pqko-discord") // Calls main package
new PqkoDiscord.EventsHandler(client, "eventFolder")
```

Now for the actual file in the "eventsFolder"

```javascript
module.exports = {
    name: "ready",
    // rest: true // client.rest.on
    // once: true // client.once Guessing it runs once
    // Default to client.on
    execute: (...args, client) => { // change ...args to the thing you want like oldMessage, newMessage
        // Code here
    }
}
```
