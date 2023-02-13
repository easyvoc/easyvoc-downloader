# Get error

{% swagger method="get" path="/getError" baseUrl="https://easyvoc-app.api.stdlib.com/easyvoc@dev" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="logId" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
  "result": {
    "ID": "provided_id",
    "Error Code": "found_code",
    "Error Message": "related_message",
    "Timestamp": "found_time"
  }
}
```
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="" %}
```json
{
  "result":"No log found with the provided ID."
}
```
{% endswagger-response %}
{% endswagger %}
