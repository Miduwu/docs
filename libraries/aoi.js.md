# Aoi.js

### JSON

Actually you can use pre-coded functions in aoi.js like `$jsonRequest` or `$httpRequest`

```
$jsonRequest[https://api.willz.repl.co/json/translate?text=Hi&source=auto&target=fr;data.translated;Error message;Authorization:YOUR_KEY]
```

### Image Manipulation

You need to install our [package](https://npmjs.com/@midowo/t-api.js) and add a ncode to your index.js

```javascript
// Setup the aoi.js bot
const aoijs = require("aoi.js")

const bot = new aoijs.Bot({...})
// Setup the T-API
const TAPI = require('@midowo/t-api.js')
const api = new TAPI.All('T-API TOKEN')
// Connect with Aoi.js
const ApiUtil = new TAPI.Util(api)
ApiUtil.connect_aoi(bot, {
    embeds: '$imageAPI', // You can change the function name
    attachments: '$attachmentAPI' // You can change the function name
})
```

#### Functions Usage:

**EMBEDS:**\
****<mark style="color:orange;">Usage:</mark> `$imageAPI[index;endpoint;JSON Params]`\
<mark style="color:purple;">Example:</mark> `$imageAPI[1;supreme;{"text": "$message"}]`

**ATTACHMENTS:**\
<mark style="color:orange;">Usage:</mark> `$attachmentAPI[endpoint;JSON Params]`\
<mark style="color:purple;">Example:</mark> `$attachmentAPI[supreme;{"text": "$message"}]`
