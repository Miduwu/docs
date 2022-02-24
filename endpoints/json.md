---
description: Full JSON endpoints list
---

# JSON

{% hint style="warning" %}
These endpoints needs the **`Authorization`** header.
{% endhint %}

{% swagger method="get" path="/owoify" baseUrl="https://api.willz.repl.co/json" summary="Owoify youw text" %}
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
text: String,
owoify: String
},
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/reverse" baseUrl="https://api.willz.repl.co/json" summary="txet ruoy esreveR" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="text" required="true" %}
Text to reverse
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: {
text: String,
reverse: String
},
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/mock" baseUrl="https://api.willz.repl.co/json" summary="mOck yOUr tExt" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="text" required="true" %}
Text to mock
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: {
text: String,
mock: String
},
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/8ball" baseUrl="https://api.willz.repl.co/json" summary="Get a random response by the magic ball" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="text" required="true" %}
Text to ask
{% endswagger-parameter %}

{% swagger-parameter in="query" name="idiom" type="String" %}
Abbreviation (es, en, pt, fr)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: {
text: String,
response: String,
language: String
},
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/translate" baseUrl="https://api.willz.repl.co/json" summary="Translate your text" %}
{% swagger-description %}
Allowed idioms: ['auto', 'af', 'sq', 'am', 'ar', 'hy', 'az', 'eu', 'be', 'bn', 'bs', 'bg', 'ca', 'ceb', 'ny', 'zh', 'zh-cn', 'zh-tw', 'co', 'hr', 'cs', 'da', 'nl', 'en', 'eo', 'et', 'tl', 'fi', 'fr', 'fy', 'gl', 'ka', 'de', 'el', 'gu', 'ht', 'ha', 'haw', 'he', 'iw', 'hi', 'hmn', 'hu', 'is', 'ig', 'id', 'ga', 'it', 'ja', 'jw', 'kn', 'kk', 'km', 'ko', 'ku', 'ky', 'lo', 'la', 'lv', 'lt', 'lb', 'mk', 'mg', 'ms', 'ml', 'mt', 'mi', 'mr', 'mn', 'my', 'ne', 'no', 'ps', 'fa', 'pl', 'pt', 'pa', 'ro', 'ru', 'sm', 'gd', 'sr', 'st', 'sn', 'sd', 'si', 'sk', 'sl', 'so', 'es', 'su', 'sw', 'sv', 'tg', 'ta', 'te', 'th', 'tr', 'uk', 'ur', 'uz', 'vi', 'cy', 'xh', 'yi', 'yo', 'zu']
{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="text" required="true" %}
Text to translate
{% endswagger-parameter %}

{% swagger-parameter in="query" name="source" type="String" required="true" %}
Abbreviation for the source idiom
{% endswagger-parameter %}

{% swagger-parameter in="query" name="target" type="String" required="true" %}
Abbreviation for the target idiom
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: {
translated: String,
source: String,
target: String
},
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/discorduser" baseUrl="https://api.willz.repl.co/json" summary="Get information about a discord user" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" type="Discord.Snowflake" name="userid" required="true" %}
User ID
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: { Discord.User },
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/npm" baseUrl="https://api.willz.repl.co/json" summary="Search a node package in npmjs.com" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="query" required="true" %}
Package name
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: {
Object
},
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/define" baseUrl="https://api.willz.repl.co/json" summary="Define a term" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="query" required="true" %}
Term to define
{% endswagger-parameter %}

{% swagger-parameter in="query" name="max" type="Number" %}
Max of items in the array
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: [Array],
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/gis" baseUrl="https://api.willz.repl.co/json" summary="Search an image in google with a query" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="query" required="true" %}
Query to get images
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: [{
url: String,
width: Number,
height: Number
}, ...],
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/playstore" baseUrl="https://api.willz.repl.co/json" summary="Search an application in playstore using the name" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="query" required="true" %}
App name
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: {
Object
},
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/weather" baseUrl="https://api.willz.repl.co/json" summary="Get the weather from a city" %}
{% swagger-description %}
quo
{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="query" required="true" %}
City to find
{% endswagger-parameter %}

{% swagger-parameter in="query" name="degree" type="String" %}
Degree type: C or F defults C
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: {
Object
},
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/quotes" baseUrl="https://api.willz.repl.co/json" summary="Get quotes from anime or reality" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="type" required="true" %}
Quote type: anime | normal
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: {
Object
},
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/ascii" baseUrl="https://api.willz.repl.co/json" summary="Ascii art of your text" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" type="String" name="text" required="true" %}
Text to asciify
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
status: 200,
data: String,
success: true
}
```
{% endswagger-response %}
{% endswagger %}
