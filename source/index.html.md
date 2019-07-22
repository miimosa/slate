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

<h1 id="miimosa-api">MiiMOSA API v1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

MiiMOSA API strives to stick to the REST convention: we use HTTP verbs such as GET, POST, PATCH and DELETE and return appropriate HTTP response codes (2xx for success, 4xx for client errors and 5xx for server errors).<br><br>We use JSON to encode all resources</p><h1 id="pagination">Pagination</h1><p>We paginate in our headers, not in our response body. This follows the proposed <a href="http://tools.ietf.org/html/rfc5988" rel="nofollow">RFC-5988</a> standard for Web linking.</p><p>

Base URLs:

* <a href="https://api.miimosa.com">https://api.miimosa.com</a>

# Authentication

* API Key (apiKey)
    - Parameter Name: **Authorization**, in: header. 

<h1 id="miimosa-api-leads">Leads</h1>

## post__leads

> Code samples

```shell
curl --request POST \
  --url https://api.miimosa.com/leads \
  --header 'authorization: string' \
  --header 'content-type: application/json' \
  --data '{"email":"string","firstname":"string","lastname":"string","phone":"string","collect_type":"string","project_description":"string","project_total_budget":"string","publication_timeframe":"string","birthdate":"string","siret":"string","post_code":"string","city":"string","project_name":"string","social_link":"string","project_crowdfunding_budget":"string","project_loan_budget":"string","project_input_budget":"string","department":"string","category":"string","turnover":"string","lead_source":"string"}'
```

```javascript
var data = JSON.stringify({
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
});

var xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener("readystatechange", function () {
  if (this.readyState === this.DONE) {
    console.log(this.responseText);
  }
});

xhr.open("POST", "https://api.miimosa.com/leads");
xhr.setRequestHeader("content-type", "application/json");
xhr.setRequestHeader("authorization", "string");

xhr.send(data);
```

`POST /leads`

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

<h3 id="post__leads-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
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

<h3 id="post__leads-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|lead created|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|invalid record|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apiKey
</aside>

<h1 id="miimosa-api-pledges">Pledges</h1>

## get__pledges

> Code samples

```shell
curl --request GET \
  --url 'https://api.miimosa.com/pledges?email=string' \
  --header 'authorization: string'
```

```javascript
var data = null;

var xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener("readystatechange", function () {
  if (this.readyState === this.DONE) {
    console.log(this.responseText);
  }
});

xhr.open("GET", "https://api.miimosa.com/pledges?email=string");
xhr.setRequestHeader("authorization", "string");

xhr.send(data);
```

`GET /pledges`

*List all valid lending pledges*

<h3 id="get__pledges-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|email|query|string|true|Search a pledges by the user's email.|
|Authorization|header|string|true|Client API key|

<h3 id="get__pledges-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|pledges listed|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|email not found|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apiKey
</aside>

<h1 id="miimosa-api-projects">Projects</h1>

## get__projects

> Code samples

```shell
curl --request GET \
  --url https://api.miimosa.com/projects \
  --header 'authorization: string'
```

```javascript
var data = null;

var xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener("readystatechange", function () {
  if (this.readyState === this.DONE) {
    console.log(this.responseText);
  }
});

xhr.open("GET", "https://api.miimosa.com/projects");
xhr.setRequestHeader("authorization", "string");

xhr.send(data);
```

`GET /projects`

*List all published projects*

<h3 id="get__projects-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|order|query|string|false|Filter projects by order type. Must be one of the order types below.|
|category|query|string|false|Category. Must be one of the categories below.|
|type|query|string|false|Type of collect for the project. Must be one of the types below.|
|region|query|string|false|Find a project by its region code. You can find codes here: <a href='https://fr.wikipedia.org/wiki/Codes_g%C3%A9ographiques_de_la_France'>link</a>.|
|keyword|query|string|false|Search a project by keyword.|
|Authorization|header|string|true|Client API key|

#### Enumerated Values

|Parameter|Value|
|---|---|
|order|populars|
|order|in_progress|
|order|recent|
|category|apiculture|
|category|alcool|
|category|aquaculture|
|category|soft|
|category|elevage|
|category|sale|
|category|sucre|
|category|horticulture|
|category|innovation|
|category|nature|
|category|lait|
|category|viticulture|
|type|donation|
|type|lending|

<h3 id="get__projects-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|projects listed|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apiKey
</aside>

<h1 id="miimosa-api-project">Project</h1>

## get__projects_{project_id}

> Code samples

```shell
curl --request GET \
  --url https://api.miimosa.com/projects/0 \
  --header 'authorization: string'
```

```javascript
var data = null;

var xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener("readystatechange", function () {
  if (this.readyState === this.DONE) {
    console.log(this.responseText);
  }
});

xhr.open("GET", "https://api.miimosa.com/projects/0");
xhr.setRequestHeader("authorization", "string");

xhr.send(data);
```

`GET /projects/{project_id}`

*Retrieve a project*

<h3 id="get__projects_{project_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|project_id|path|integer|true|Id of the project|
|Authorization|header|string|true|Client API key|

<h3 id="get__projects_{project_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|project retrieved|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|project not found|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apiKey
</aside>

<h1 id="miimosa-api-wallet">Wallet</h1>

## get__wallet

> Code samples

```shell
curl --request GET \
  --url 'https://api.miimosa.com/wallet?email=string' \
  --header 'authorization: string'
```

```javascript
var data = null;

var xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener("readystatechange", function () {
  if (this.readyState === this.DONE) {
    console.log(this.responseText);
  }
});

xhr.open("GET", "https://api.miimosa.com/wallet?email=string");
xhr.setRequestHeader("authorization", "string");

xhr.send(data);
```

`GET /wallet`

*Retrieve a user's wallet thanks to his email*

<h3 id="get__wallet-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|email|query|string|true|Search a wallet by the user's email.|
|Authorization|header|string|true|Client API key|

<h3 id="get__wallet-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|wallet retrieved|None|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|wallet not found|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apiKey
</aside>

