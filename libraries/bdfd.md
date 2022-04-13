---
description: How to use our API in Bot Designer For Discord
---

# 🤮 BDFD

### JSON

To use our JSON endpoints its very easy, you need to know how to use `$httpAddHeader`, `$httpGet` and `$httpResult`

**Example:**

```
$nomention
$httpAddHeader[Authorization;YOUR_API_KEY]
$httpGet[https://api.willz.repl.co/json/translate?text=Hello&source=auto&target=fr]

$httpResult[data;translated]
```

### Image Manipulation

Agh... check this:

{% content-ref url="../extra/imgur.md" %}
[imgur.md](../extra/imgur.md)
{% endcontent-ref %}

{% hint style="info" %}
Consider learning Aoi.js instead.
{% endhint %}

You also can use the link from public group directly.

Ex: [https://api.miduwu.ga/public/discordjs?text=T-API](https://api.miduwu.ga/public/discordjs?text=T-API)

![](https://api.miduwu.ga/public/discordjs?text=T-API)
