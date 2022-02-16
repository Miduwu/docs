# Anime

{% hint style="warning" %}
These endpoints needs the **`Authorization`** header.
{% endhint %}

{% swagger method="get" path="/reaction" baseUrl="https://api.willz.repl.co/anime" summary="Get a random gif about a type." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="type" type="String" required="true" %}
Name of the type
{% endswagger-parameter %}

{% swagger-parameter in="query" name="source" type="Number" %}
Number of the source, defaults 1
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
status: 200,
data: String,
success: true
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/search" baseUrl="https://api.willz.repl.co/anime" summary="Search a manga/anime" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="type" type="String" required="true" %}
Content type: anime | manga
{% endswagger-parameter %}

{% swagger-parameter in="query" name="query" type="String" required="true" %}
The manga/anime title
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
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

{% swagger method="get" path="/neko" baseUrl="https://api.willz.repl.co/anime" summary="Get a random gif about a type." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="type" type="String" required="true" %}
Content type: image | gif
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
status: 200,
data: String,
success: true
}
```
{% endswagger-response %}
{% endswagger %}
