---
description: The required setup for the web server ( Express )
---

# Basic Setup

Calling Express and getting the actual Core

```javascript
const { client_id, client_secret, token } = require("./config.json") 
const OAuth2Link = "..."

const PqkoDiscord = require("pqko-discord")
const OAuth2 = new PqkoDiscord.OAuth2(client_id, client_secret, token, "http://localhost:8000/...")
const auth = new PqkoDiscord.Auth.DiscordAuth(OAuth2)

const express = require("express")
const app = express()

app.listen(8000, () => {
  console.log("🚀 Listening on port 8000!")
  console.log("http://localhost:8000")
})

app.get("/", (req, res) => {
  res.send("Welcome to pqko-discord!")
})
```
