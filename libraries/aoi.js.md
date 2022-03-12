# Aoi.js

### JSON

Actually you can use pre-coded functions in aoi.js like `$jsonRequest` or `$httpRequest` or the package extension (You need to install our [package](https://npmjs.com/@midowo/t-api.js) and add a code to your index.js)

**Using `$jsonRequest` from aoi.js**

```
$jsonRequest[https://api.willz.repl.co/json/translate?text=Hi&source=auto&target=fr;data.translated;Error message;Authorization:YOUR_KEY]
```

**Using `$requestAPI` from our package (very recomended)**

```
$getProperty[data.translated]
$requestAPI[json;translate;{"text": Hi", "source": "auto", "target": "fr"};Something went wrong]
```

### Image Manipulation

You need to install our [package](https://npmjs.com/@midowo/t-api.js) and add a code to your index.js

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
    attachments: '$attachmentAPI', // You can change the function name
    objects: '$requestAPI', // You can change the function name
    result: '$getProperty' // You can change the function name
})
```

#### Functions Usage:

**EMBEDS:**\
<mark style="color:orange;">Usage:</mark> `$imageAPI[index;endpoint;JSON Params;name.ext]`\
<mark style="color:purple;">Example:</mark> `$imageAPI[1;supreme;{"text": "$message"};canvas.png]`

**ATTACHMENTS:**\
<mark style="color:orange;">Usage:</mark> `$attachmentAPI[endpoint;JSON Params;name.ext]`\
<mark style="color:purple;">Example:</mark> `$attachmentAPI[supreme;{"text": "$message"};canvas.png]`

**OBJECTS (JSON):**\
<mark style="color:orange;">Usage:</mark> `$requestAPI[group(anime/json);endpoint;JSON Params;error]`\
<mark style="color:purple;">Example:</mark> `$requestAPI[json;quotes;{"type": "anime"};Something went wrong]`

**OBJECTS RESULT (JSON):**\
<mark style="color:orange;">Usage:</mark> `$getProperty[property/$defaut for all json]`\
<mark style="color:purple;">Example:</mark> `$getProperty[data.quote]`
