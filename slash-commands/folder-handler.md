---
description: >-
  The folder handler is the recommended handler when it comes to organizing
  files
---

# Folder Handler

The folder handler is as easy as the JSON Handler to setup and use! Make sure you set "commands" to where your commands folder is remember we use PWD (Process Working Directory). So if you run this from a src and your commands is one back it should look something like this "../commands"

```javascript
pqko.folderHandler("commands")
```

In the commands folder you can create as many sub-folders and the handler will still detect the JS files! To set the actual commands up properly use this small template to get the hang of it

```javascript
const { SlashCommandBuilder } = require('discord.js')

module.exports = {
    data: new SlashCommandBuilder().setName("test").setDescription("This is the first command with pqko-discord!"),
    execute: async (interaction, client) => {
        await interaction.reply("This has been sent via pqko-discord module!")
    }
}
```

But intellisense doesn't work so with a bit of extra code can add that feature back

```javascript
const { SlashCommandBuilder, AutocompleteInteraction, Client } = require('discord.js')

module.exports = {
    data: new SlashCommandBuilder().setName("test").setDescription("This is the first command with pqko-discord!"),
    /**
    *
    * @param {AutocompleteInteraction} interaction
    * @param {Client} client
    */
    execute: async (interaction, client) => {
        await interaction.reply("This has been sent via pqko-discord module!")
    }
}
```

That's it.
