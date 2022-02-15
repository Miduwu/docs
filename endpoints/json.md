---
description: Full JSON endpoints list
---

# JSON

{% swagger method="get" path="/owoify" baseUrl="https://api.willz.repl.co/json" summary="Owoify your text" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="text" required="true" %}
Text to owoifize
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: {
text: "",
owoify: ""
}
}
```
{% endswagger-response %}
{% endswagger %}
