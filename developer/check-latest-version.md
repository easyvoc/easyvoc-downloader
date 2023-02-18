# Check latest version

{% swagger method="get" path="" baseUrl="https://easyvoc-app.api.stdlib.com/easyvoc@dev/" summary="Check if your version is up to date" expanded="false" %}
{% swagger-description %}
With this API, you can check if the send version is the latest.


{% endswagger-description %}

{% swagger-parameter in="path" name="receivedNumber" required="true" type="Integer" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```json
{
  "result":true
}
```
{% endswagger-response %}

{% swagger-response status="204: No Content" description="" %}
```json
{
  "result":false
}
```
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="" %}
```json
{
  "result":false
}
```
{% endswagger-response %}
{% endswagger %}

<details>

<summary>Send API request (Python)</summary>

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

<details>

<summary>Send API request (Javascript)</summary>

```javascript
const request = require("request");

function sendRequestToAPI(receivedNumber) {
  const API_ENDPOINT = `https://easyvoc-app.api.stdlib.com/easyvoc@dev/?receivedNumber=${receivedNumber}`;
  return new Promise((resolve, reject) => {
    request(API_ENDPOINT, (error, response, body) => {
      if (error) {
        reject(error);
      } else {
        resolve(JSON.parse(body));
      }
    });
  });
}

async function main() {
  const receivedNumber = Number(prompt("Enter a number:"));
  const result = await sendRequestToAPI(receivedNumber);
  if (result.result) {
    console.log("Result from API: True");
  } else {
    console.log("Result from API: False");
  }
}

main();

```

</details>

{% hint style="danger" %}
**The following sample code is provided for demonstration purposes only and is not intended to be used in production. It is the sole responsibility of the user to ensure that the code is correct, secure, and meets the specific requirements of their application. The authors and publishers of this API documentation make no representations or warranties of any kind, express or implied, about the completeness, accuracy, reliability, suitability or availability with respect to the sample code and related information contained in this documentation. Any use of the sample code is done at the user's own risk and the authors and publishers of this API documentation will not be liable for any damages of any nature arising from its use.**
{% endhint %}

