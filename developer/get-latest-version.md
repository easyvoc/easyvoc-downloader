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
**The following sample code is provided for demonstration purposes only and is not intended to be used in production. It is the sole responsibility of the user to ensure that the code is correct, secure, and meets the specific requirements of their application. The authors and publishers of this API documentation make no representations or warranties of any kind, express or implied, about the completeness, accuracy, reliability, suitability or availability with respect to the sample code and related information contained in this documentation. Any use of the sample code is done at the user's own risk and the authors and publishers of this API documentation will not be liable for any damages of any nature arising from its use.**
{% endhint %}
