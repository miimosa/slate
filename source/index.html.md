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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|lead created|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|invalid record|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
apiKey
</aside>

