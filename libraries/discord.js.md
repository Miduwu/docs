---
description: How to use our API in discord.js
---

# Discord.js

There is two ways to use T-API in discord.js, both are good options.

### Using the package (recomended)

You can use our [package](https://npmjs.com/@midowo/t-api.js) and add that property to your client definition.

```javascript
const Discord = require('discord.js')
const client = new Discord.Client({...})

const TAPI = require('@midowo/t-api.js') // npm i
client.tapi = new TAPI.All('T-API_TOKEN')

client.on('interactionCreate', async interaction => {
if(interaction.isCommand() && interaction.commandName === 'tweet') {
const buff = await client.tapi.image.tweet({
text: interaction.options.getString('message'),
username: interaction.user.username,
image: interaction.user.displayAvatarURL()
})
interaction.reply({files: [new Discord.MessageAttachment(buff, 'file.png')]})
}
})

client.login('TOKEN')
```

### Using axios

You can use any http requests package, we recomend you to use axios.

```javascript
const Discord = require('discord.js')
const axios = require('axios') // npm i

const client = new Discord.Client({...})

client.on('interactionCreate', async interaction => {
if(interaction.isCommand() && interaction.commandName === 'tweet') {
const buff = await axios.get(`https://api.willz.repl.co/image/tweet?text=${interaction.options.getString('message')}&username=${interaction.user.username}&image=${interaction.user.displayAvatarURL()}`, {
headers: {"Authorization": "YOUR_KEY"},
responseType: 'arraybuffer'
})
interaction.reply({files: [new Discord.MessageAttachment(buff, 'file.png')]})
}
})

client.login('TOKEN')
```
