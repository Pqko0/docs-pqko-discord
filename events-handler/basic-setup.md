---
description: The required setup
---

# Basic Setup

Its actually surprisingly small for what its actually meant for the event handler to work

<pre class="language-javascript"><code class="lang-javascript">const { client_id, client_secret, token } = require("./config.json")

const { Client } = require("discord.js")
const client = new Client({ intents: [] }); // The intents might not be correct...

const PqkoDiscord = require("pqko-discord") // Calls main package
<strong>const events = new PqkoDiscord.EventsHandler(client, "eventFolder")
</strong><strong>events.event()
</strong></code></pre>

Now for the actual file(s) in the "eventsFolder"

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
