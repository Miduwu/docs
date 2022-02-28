---
description: Information about the wrapper package
---

# Package

We have an API wrapper, its the better way to interact with T-API.

{% embed url="https://npmjs.com/package/@midowo/t-api.js" %}
Open npmjs.com
{% endembed %}

### Install

```
npm i @midowo/t-api.js
```

### Using with discord.js

{% code title="index.js" %}
```javascript
const { Client, Intents } = require('discord.js')
const TAPI = require('@midowo/t-api.js')

const client = new Client({ intents: [Intents.FLAGS.GUILDS] });
client.tapi = new TAPI.All('YOUR_API_KEY'); // Join the support server to get one

client.login(token);
```
{% endcode %}

{% code title="command.js" %}
```javascript
const { MessageAttachment } = require('discord.js')
module.exports = {
    // your slash options,
    async execute(interaction, client) {
    
    const buff = await client.tapi.image.tweet({
    image: interaction.user.displayAvatarURL(),
    text: 'Hello world!',
    username: interaction.user.username
    });
    const attachment = new MessageAttachment(buff, 'image.png')
    interaction.reply({files: [attachment]})
    }
}
```
{% endcode %}

### Classes

\
**`All`** This class has all endpoints inside 3 json keys (groups): `json`, `image`, `anime,` those has the corresponding endpoints in each one.\
<mark style="color:red;">**USAGE:**</mark> `<Class Attribute>.group.endpoint()`

**Json** This class only has the JSON endpoints.\
<mark style="color:red;">**USAGE:**</mark> `<Class Attribute>.endpoint()`

**`Image`** This class only has the Buffer endpoints.\
<mark style="color:red;">**USAGE:**</mark> `<Class Attribute>.endpoint()`

**`Anime`** This class only has the Anime endpoints.\
<mark style="color:red;">**USAGE:**</mark> `<Class Attribute>.endpoint()`

**`Util`** This class has util methods, check [aoi.js guide](../libraries/aoi.js.md).\
<mark style="color:red;">**USAGE:**</mark> `<Class Attribute>.method()`

### Available endpoints

[Check all endpoints clicking here!](https://github.com/Miduwu/T-API.js/blob/main/auxiliar/endpoints.json)

### Contribute us

{% embed url="https://github.com/Miduwu/T-API.js" %}
Check github
{% endembed %}
