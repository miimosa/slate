---
title: MiiMOSA API
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<h1 id="MiiMOSA-API">MiiMOSA API v1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

MiiMOSA API strives to stick to the REST convention: we use HTTP verbs such as GET, POST, PATCH and DELETE and return appropriate HTTP response codes (2xx for success, 4xx for client errors and 5xx for server errors).<br><br>We use JSON to encode all resources</p><h1 id="pagination">Pagination</h1><p>We paginate in our headers, not in our response body. This follows the proposed <a href="http://tools.ietf.org/html/rfc5988" rel="nofollow">RFC-5988</a> standard for Web linking.</p><p>

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
  -H 'Authorization: string' \
  -H 'Authorization: API_KEY'

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
  'Authorization':'string',
  'Authorization':'API_KEY'

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

`POST /api/leads`

*Creates a lead*

> Body parameter

```json
{
  "email": "string",
  "firstname": "string",
  "lastname": "string",
  "phone": "string",
  "collect_type": "string",
  "project_description": "string",
  "project_total_budget": "string",
  "publication_timeframe": "string",
  "birthdate": "string",
  "siret": "string",
  "post_code": "string",
  "city": "string",
  "project_name": "string",
  "social_link": "string",
  "project_crowdfunding_budget": "string",
  "project_loan_budget": "string",
  "project_input_budget": "string",
  "department": "string",
  "category": "string",
  "turnover": "string",
  "lead_source": "string"
}
```

<h3 id="post__api_leads-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Client API key|
|body|body|object|false|none|
|» email|body|string|true|Email address.|
|» firstname|body|string|true|First name.|
|» lastname|body|string|true|Last name.|
|» phone|body|string|true|Phone number.|
|» collect_type|body|string|true|Collect type. Must be <b>donation</b> or <b>lending</b>.|
|» project_description|body|string|true|Description of the project.|
|» project_total_budget|body|string|true|Total budget of the project.|
|» publication_timeframe|body|string|true|Publication timeframe. Must be <b>within_month</b>, <b>next_months</b> or <b>another_quarter</b>.|
|» birthdate|body|string|false|Birthdate. No specific format.|
|» siret|body|string|false|Siret.|
|» post_code|body|string|false|Zip code.|
|» city|body|string|false|City.|
|» project_name|body|string|false|Project name.|
|» social_link|body|string|false|Social link like facebook, twitter and so on.|
|» project_crowdfunding_budget|body|string|false|none|
|» project_loan_budget|body|string|false|none|
|» project_input_budget|body|string|false|none|
|» department|body|string|false|Department code|
|» category|body|string|false|Category. Must be on of the following categories: <b>apiculture</b> <b>aquaculture</b> <b>alcool</b> <b>soft</b> <b>elevage</b> <b>sale</b> <b>sucre</b> <b>horticulture</b> <b>innovation</b> <b>nature</b> <b>lait</b> <b>viticulture</b>.|
|» turnover|body|string|false|Turnover.|
|» lead_source|body|string|false|The source of the lead.|

<h3 id="post__api_leads-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|lead created|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|invalid record|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apiKey
</aside>

<h1 id="MiiMOSA-API-Projects">Projects</h1>

## get__api_projects

> Code samples

```shell
# You can also use wget
curl -X GET ///api/projects \
  -H 'Content-Type: application/json' \
  -H 'Authorization: string' \
  -H 'Authorization: API_KEY'

```

```http
GET ///api/projects HTTP/1.1
Host: null
Content-Type: application/json

Authorization: string

```

```javascript
var headers = {
  'Content-Type':'application/json',
  'Authorization':'string',
  'Authorization':'API_KEY'

};

$.ajax({
  url: '///api/projects',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

`GET /api/projects`

*List all published projects*

> Body parameter

```json
[
  {
    "url": "string"
  }
]
```

<h3 id="get__api_projects-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Client API key|
|body|body|array[object]|false|none|

<h3 id="get__api_projects-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|projects listed|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apiKey
</aside>

