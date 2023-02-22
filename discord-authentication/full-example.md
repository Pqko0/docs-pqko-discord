---
description: The ending
---

# Full Example

This is how it should look like

```javascript
const { client_id, client_secret, token } = require("./config.json") 
const OAuth2Link = "..."

const PqkoDiscord = require("pqko-discord")
const OAuth2 = new PqkoDiscord.OAuth2(client_id, client_secret, token, "http://localhost:8000/login")
const auth = new PqkoDiscord.Auth.DiscordAuth(OAuth2)

const express = require("express")
const app = express()

app.listen(8000, () => {
  console.log("🚀 Listening on port 8000!")
  console.log("http://localhost:8000")
})

app.use(PqkoDiscord.Auth.cookieparser())
app.use(auth.__express(OAuth2))

app.get("/", (req, res) => {
  res.send("Welcome to pqko-discord!")
})

app.get("/login", async (req, res) => {
    if(req.logged == true) return res.redirect("/dashboard")

    if(req.query.code) {
        const x = await auth.login(req, res)

        if(x.message == 1 && x.account == 1) {
            res.cookie("token", x.token)

            return res.redirect("/dashboard");
        } else return res.redirect(OAuth2Link)
    } else return res.redirect(OAuth2Link)
})
app.get("/logout", (req, res) => {
    if(req.logged == false) return res.redirect("/")

    auth.logout(req, res) // Passes nothing back
    return res.redirect("/")
})
app.get("/dashboard", (req, res) => {
    res.send(req.user)
})
```
