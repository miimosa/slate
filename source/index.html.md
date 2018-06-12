---
title: MiiMOSA API
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - javascript--nodejs: Node.JS
  - ruby: Ruby
  - python: Python
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="MiiMOSA-API">MiiMOSA API v1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

<h1 id="MiiMOSA-API-Leads">Leads</h1>

## post__api_v1_leads

> Code samples

```shell
# You can also use wget
curl -X POST ///api/v1/leads \
  -H 'Content-Type: application/json'

```

```http
POST ///api/v1/leads HTTP/1.1
Host: null
Content-Type: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json'

};

$.ajax({
  url: '///api/v1/leads',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "firstname": "string",
  "lastname": "string"
}';
const headers = {
  'Content-Type':'application/json'

};

fetch('///api/v1/leads',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json'
}

result = RestClient.post '///api/v1/leads',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json'
}

r = requests.post('///api/v1/leads', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("///api/v1/leads");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "///api/v1/leads", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v1/leads`

*Creates a lead*

> Body parameter

```json
{
  "firstname": "string",
  "lastname": "string"
}
```

<h3 id="post__api_v1_leads-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» firstname|body|string|true|none|
|» lastname|body|string|true|none|

<h3 id="post__api_v1_leads-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|lead created|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|invalid request|None|

<aside class="success">
This operation does not require authentication
</aside>

