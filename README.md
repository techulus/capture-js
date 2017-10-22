[![N|Solid](https://s3-ap-southeast-1.amazonaws.com/capture-techulus/logo.png)](https://capture.techulus.in/)

# Capture JavaScript

Get your API Key and Secret from https://capture.techulus.in/console

```javascript
// Include https://github.com/blueimp/JavaScript-MD5

var API_URL = 'https://api.capture.techulus.in/';
var your_api_key = 'API_KEY_FROM_CONSOLE';
var your_api_secret = 'API_SECRET_FROM_CONSOLE'

// Target URL
var input_url = encodeURIComponent('http://techulus.in/');
var hash = md5(your_api_secret + 'url=' + input_url);

// Image URL
var result_img_url = API_URL + your_api_key + '/' + hash + '/image?url=' + input_url;
// PDF URL
var result_pdf_url = API_URL + your_api_key + '/' + hash + '/pdf?url=' + input_url;

console.log(result_img_url, result_pdf_url);
```
