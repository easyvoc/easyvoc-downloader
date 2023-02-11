# Get latest version

{% swagger method="get" path="/version" baseUrl="https://easyvoc-app.api.stdlib.com/easyvoc@dev" summary="Get the latest EasyVoc version" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
```json
{
  "version": 8
}
```
{% endswagger-response %}
{% endswagger %}

<details>

<summary>Send API request (Python)</summary>

```python
import requests

def get_info_from_api():
    API_ENDPOINT = "https://easyvoc-app.api.stdlib.com/easyvoc@dev/version/"
    response = requests.get(API_ENDPOINT)
    return response.json()

if __name__ == '__main__':
    result = get_info_from_api()
    print(result)

```

</details>

<details>

<summary>Send API request (Javascript)</summary>

```javascript
fetch("https://easyvoc-app.api.stdlib.com/easyvoc@dev/version/")
.then(response => response.json())                                                                        
.then(data => {
  console.log(data);
})
.catch(error => console.error(error));

```

</details>

{% hint style="danger" %}
These are just examples!!!
{% endhint %}
