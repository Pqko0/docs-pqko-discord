---
description: This type of handler is good for AIO (All In One)
---

# JSON Handler

JSON Handler comes with a quick setup which is good for quick/small projects. These are not known as they are hard to come by and are annoying or it will make it look messy to setup in one file&#x20;

This is the basic setup for a JSON Handler

```javascript
const { SlashCommandBuilder } = require('discord.js')

const commands = [
    {
        data: new SlashCommandBuilder().setName("test").setDescription("This is the first command with pqko-discord!"),
        execute: async (interaction, client) => {
            await interaction.reply("This has been sent via pqko-discord module!")
        }
    }
]

pqko.jsonHandler(commands)
```

Now we can't forget the intellisense, probably the best part.

```javascript
const { SlashCommandBuilder, AutocompleteInteraction, Client } = require('discord.js')

const commands = [
    {
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
]

pqko.jsonHandler(commands)
```

Now just stack the JSON to create multiple commands like this.

```javascript
const { SlashCommandBuilder } = require('discord.js')

const commands = [
    {
        data: new SlashCommandBuilder().setName("test").setDescription("This is the first command with pqko-discord!"),
        execute: async (interaction, client) => {
            await interaction.reply("This has been sent via pqko-discord module!")
        }
    },
    {
        data: new SlashCommandBuilder().setName("hello").setDescription("The second command on JSON Handler"),
        execute: async (interaction, client) => {
            await interaction.reply("This is the 2nd command!")
        }
    }
]

pqko.jsonHandler(commands)
```

As simple as that
