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

<details>

<summary>Send API request</summary>

{% code lineNumbers="true" %}
```python
import requests

def send_request_to_api(receivedNumber):
    API_ENDPOINT = f"https://easyvoc-app.api.stdlib.com/easyvoc@dev/?receivedNumber={receivedNumber}"
    response = requests.get(API_ENDPOINT)
    return response.json()

if __name__ == '__main__':
    receivedNumber = int(input("Enter a number: "))
    result = send_request_to_api(receivedNumber)
    if result['result']:
        print("Result from API: True")
    else:
        print("Result from API: False")
```
{% endcode %}

</details>
