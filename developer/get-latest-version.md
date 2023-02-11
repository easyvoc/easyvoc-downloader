# Get latest version

{% swagger method="post" path="?receivedNumber=" baseUrl="https://easyvoc-app.api.stdlib.com/easyvoc@dev/" summary="Check if your version is up to date" %}
{% swagger-description %}
With this API, you can check if the send version is the latest.
{% endswagger-description %}

{% swagger-parameter in="path" name="receivedNumber" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{"result":true}
```
{% endswagger-response %}

{% swagger-response status="204: No Content" description="" %}
```javascript
{"result":false}
```
{% endswagger-response %}
{% endswagger %}
