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

MiiMOSA API strives to stick to the REST convention: we use HTTP verbs such as GET, POST, PATCH and DELETE and return appropriate HTTP response codes (2xx for success, 4xx for client errors and 5xx for server errors).<br><br>We use JSON to encode all resources

# Authentication

* API Key (apiKey)
    - Parameter Name: **Authorization**, in: header. 

<h1 id="MiiMOSA-API-Leads">Leads</h1>

## post__api_leads

> Code samples

```shell
# You can also use wget
curl -X POST ///api/leads \
  -H 'Content-Type: application/json' \
  -H 'Authorization: string'

```

```http
POST ///api/leads HTTP/1.1
Host: null
Content-Type: application/json

Authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Authorization':'string'

};

$.ajax({
  url: '///api/leads',
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
  "lastname": "string",
  "birthdate": "string",
  "email": "string",
  "siret": "string",
  "phone": "string",
  "post_code": "string",
  "city": "string",
  "project_name": "string",
  "project_description": "string",
  "social_link": "string",
  "project_total_budget": "string",
  "project_crowdfunding_budget": "string",
  "project_loan_budget": "string",
  "project_input_budget": "string",
  "department": "string",
  "type": "string",
  "category": "string",
  "financial_type": "string",
  "user_id": "string",
  "status": "string",
  "estimated_publication_at": "string",
  "partner_id": "string",
  "custom_fields": "string",
  "category_id": "string",
  "turnover": "string",
  "project_id": "string",
  "team_user_id": "string",
  "collect_type": "string",
  "publication_timeframe": "string",
  "lead_source": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Authorization':'string'

};

fetch('///api/leads',
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
  'Content-Type' => 'application/json',
  'Authorization' => 'string'
}

result = RestClient.post '///api/leads',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Authorization': 'string'
}

r = requests.post('///api/leads', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("///api/leads");
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
        "Authorization": []string{"string"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "///api/leads", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/leads`

*Creates a lead*

> Body parameter

```json
{
  "firstname": "string",
  "lastname": "string",
  "birthdate": "string",
  "email": "string",
  "siret": "string",
  "phone": "string",
  "post_code": "string",
  "city": "string",
  "project_name": "string",
  "project_description": "string",
  "social_link": "string",
  "project_total_budget": "string",
  "project_crowdfunding_budget": "string",
  "project_loan_budget": "string",
  "project_input_budget": "string",
  "department": "string",
  "type": "string",
  "category": "string",
  "financial_type": "string",
  "user_id": "string",
  "status": "string",
  "estimated_publication_at": "string",
  "partner_id": "string",
  "custom_fields": "string",
  "category_id": "string",
  "turnover": "string",
  "project_id": "string",
  "team_user_id": "string",
  "collect_type": "string",
  "publication_timeframe": "string",
  "lead_source": "string"
}
```

<h3 id="post__api_leads-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Client API key|
|body|body|object|false|none|
|» firstname|body|string|true|none|
|» lastname|body|string|true|none|
|» birthdate|body|string|false|none|
|» email|body|string|true|none|
|» siret|body|string|false|none|
|» phone|body|string|true|none|
|» post_code|body|string|false|none|
|» city|body|string|false|none|
|» project_name|body|string|false|none|
|» project_description|body|string|true|none|
|» social_link|body|string|false|none|
|» project_total_budget|body|string|true|none|
|» project_crowdfunding_budget|body|string|false|none|
|» project_loan_budget|body|string|false|none|
|» project_input_budget|body|string|false|none|
|» department|body|string|false|none|
|» type|body|string|false|none|
|» category|body|string|false|none|
|» financial_type|body|string|false|none|
|» user_id|body|string|false|none|
|» status|body|string|false|none|
|» estimated_publication_at|body|string|false|none|
|» partner_id|body|string|false|none|
|» custom_fields|body|string|false|none|
|» category_id|body|string|false|none|
|» turnover|body|string|false|none|
|» project_id|body|string|false|none|
|» team_user_id|body|string|false|none|
|» collect_type|body|string|true|none|
|» publication_timeframe|body|string|true|none|
|» lead_source|body|string|false|none|

<h3 id="post__api_leads-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|lead created|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|invalid request|None|

<aside class="success">
This operation does not require authentication
</aside>

