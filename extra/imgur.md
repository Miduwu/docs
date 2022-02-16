---
description: Imgur allows you to keep using our image endpoints in BDFD
---

# Imgur

First of all, this page **only** applies to **BDFD users**.

Image manipulation endpoints <mark style="color:red;">**are not**</mark> intended to be used in a mobile app that facilitates the Discord bot creation, so we recommend trying to use [aoi.js](https://www.npmjs.com/package/aoi.js) or [discord.js](https://www.npmjs.com/package/discord.js)

Due to the high demand for these endpoints in this ~~trash~~ application, we have been forced to make an endpoint that facilitates a possible interaction with our endpoints in this app, so <mark style="color:green;">**IT IS ALREADY POSSIBLE TO USE IMAGE ENDPOINTS IN BDFD.**</mark>

### How to use?

First, you need to create a **IMGUR API ACCOUNT**, go to [https://api.imgur.com/oauth2/addclient](https://api.imgur.com/oauth2/addclient)\
Now you need to write that data and make sure you select the **OAuth 2 authorization without a callback URL**.\
![](<../.gitbook/assets/image (1).png>)

Now click on <mark style="color:green;">**SUBMIT**</mark> and... **COPY YOUR CLIENT ID** (You must keep this ID in a safe place)

To use the image endpoints you need to use a second endpoint:\
<mark style="color:purple;">**https://api.willz.repl.co/json/resolvebuffer**</mark>

| Parameter Name |                         Description                         |
| :------------: | :---------------------------------------------------------: |
|     client     |          Your **IMGUR CLENT ID**, the one you saved         |
|      body      | The image endpoint URL, but you will use `AAND` instead `&` |

### Examples

**TWEET COMMAND**

```
$nomention
$c[Our API key, not IMGUR related]
$httpAddHeader[Authorization;YOUR_API_KEY]
$httpGet[https://api.willz.repl.co/json/resolvebuffer?client=MYIMGURID&body=https://api.willz.rep].co/image/tweet?username=$usernameAANDtext=$messageAANDDimage=$authorAvatar
```

