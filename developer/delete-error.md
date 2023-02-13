# Delete error

{% swagger method="delete" path="/deleteError" baseUrl="https://easyvoc-app.api.stdlib.com/easyvoc@dev" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
    "deleted":true
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```json
{
  "error": {
    "type": "ParameterError",
    "message": "One or more parameters were invalid or missing from your request.",
    "details": {
      "logId": {
        "message": "required",
        "required": true
      }
    }
  }
}
```
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="" %}
```json
{
    "deleted":false
}
```
{% endswagger-response %}
{% endswagger %}
