---
title: Grassrootz API
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

<h1 id="Grassrootz-API">Grassrootz API v1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="//api.dev.grassrootz.com/">//api.dev.grassrootz.com/</a>

# Authentication

* API Key (ApiKeyHeader)
    - Parameter Name: **ApiKey**, in: header. Application API Key

* API Key (SessionKeyQuery)
    - Parameter Name: **Authorization**, in: header. Authorization Token

<h1 id="Grassrootz-API-AccessKey">AccessKey</h1>

## ApiV2AccessKeyByIdGet

<a id="opIdApiV2AccessKeyByIdGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/AccessKey/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/AccessKey/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/AccessKey/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/AccessKey/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/AccessKey/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/AccessKey/{id}`

*Gets a key object by id*

<h3 id="apiv2accesskeybyidget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Donation id|

> Example responses

> 200 Response

```json
{
  "data": {
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "clientKey": "string",
    "description": "string",
    "createdAt": "2018-08-20T06:00:18Z"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accesskeybyidget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_AccessKeyElementModel_](#schemascalaractionresult_accesskeyelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_AccessKeyElementModel_](#schemascalaractionresult_accesskeyelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccessKeyByIdPut

<a id="opIdApiV2AccessKeyByIdPut"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT //api.dev.grassrootz.com//api/v2/AccessKey/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PUT //api.dev.grassrootz.com//api/v2/AccessKey/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "organizationId": 0,
  "description": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
{
  method: 'PUT',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.put '//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.put('//api.dev.grassrootz.com//api/v2/AccessKey/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/AccessKey/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "//api.dev.grassrootz.com//api/v2/AccessKey/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v2/AccessKey/{id}`

*Updates a donation key by id*

> Body parameter

```json
{
  "organizationId": 0,
  "description": "string"
}
```

<h3 id="apiv2accesskeybyidput-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the donation object being modified|
|body|body|[AccessKeyEditModel](#schemaaccesskeyeditmodel)|false|The donation model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "clientKey": "string",
    "description": "string",
    "createdAt": "2018-08-20T06:00:18Z"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accesskeybyidput-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_AccessKeyElementModel_](#schemascalaractionresult_accesskeyelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_AccessKeyElementModel_](#schemascalaractionresult_accesskeyelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccessKeyByIdDelete

<a id="opIdApiV2AccessKeyByIdDelete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE //api.dev.grassrootz.com//api/v2/AccessKey/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
DELETE //api.dev.grassrootz.com//api/v2/AccessKey/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
{
  method: 'DELETE',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.delete '//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.delete('//api.dev.grassrootz.com//api/v2/AccessKey/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/AccessKey/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "//api.dev.grassrootz.com//api/v2/AccessKey/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/AccessKey/{id}`

*Patches (partial update) a key object by id*

<h3 id="apiv2accesskeybyiddelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the donation object being modified|

> Example responses

> 200 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accesskeybyiddelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccessKeyByIdPatch

<a id="opIdApiV2AccessKeyByIdPatch"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH //api.dev.grassrootz.com//api/v2/AccessKey/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PATCH //api.dev.grassrootz.com//api/v2/AccessKey/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
  method: 'patch',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
{
  method: 'PATCH',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.patch '//api.dev.grassrootz.com//api/v2/AccessKey/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.patch('//api.dev.grassrootz.com//api/v2/AccessKey/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/AccessKey/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "//api.dev.grassrootz.com//api/v2/AccessKey/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v2/AccessKey/{id}`

*Patches (partial update) a key object by id*

> Body parameter

```json
[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]
```

<h3 id="apiv2accesskeybyidpatch-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the donation object being modified|
|body|body|[OperationArray](#schemaoperationarray)|false|The donation model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "accountId": 0,
    "amount": 0,
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string",
      "template": {
        "key": "string",
        "value": {}
      }
    },
    "donatedAtLocal": "2018-08-20T06:00:18Z",
    "donatedAt": "2018-08-20T06:00:18Z",
    "donor": {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "anonymous": true,
      "businessName": "string",
      "donorId": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "newsletter": true,
      "phoneNumber": "string"
    },
    "financials": {
      "cardBrand": "string",
      "cardCountry": "string",
      "cardLast4Digits": "string",
      "currency": "string",
      "fee": 0,
      "feeCovered": true,
      "platform": "stripe",
      "refunded": true,
      "refundedAt": "2018-08-20T06:00:18Z",
      "refundedAtLocal": "2018-08-20T06:00:18Z",
      "subscription": true,
      "tax": 0,
      "totalFees": 0,
      "timezone": "string"
    },
    "fundraiserId": 0,
    "fundraiser": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAt": "2018-08-20T06:00:18Z",
    "message": "string",
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "pageType": "campaign",
    "receiptNumber": "string",
    "reply": {
      "displayFirstName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "repliedAtLocal": "2018-08-20T06:00:18Z",
      "repliedAt": "2018-08-20T06:00:18Z",
      "reply": "string"
    },
    "status": "collectedFromCustomer",
    "teamId": 0,
    "team": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "type": "online"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accesskeybyidpatch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccessKeyPost

<a id="opIdApiV2AccessKeyPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/AccessKey \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/AccessKey HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/AccessKey',
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
  "organizationId": 0,
  "description": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/AccessKey',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/AccessKey',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/AccessKey', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/AccessKey");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/AccessKey", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/AccessKey`

*Creates a new access key*

> Body parameter

```json
{
  "organizationId": 0,
  "description": "string"
}
```

<h3 id="apiv2accesskeypost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccessKeyEditModel](#schemaaccesskeyeditmodel)|false|The donation model containing the details|

> Example responses

> 201 Response

```json
{
  "data": {
    "accountId": 0,
    "amount": 0,
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string",
      "template": {
        "key": "string",
        "value": {}
      }
    },
    "donatedAtLocal": "2018-08-20T06:00:18Z",
    "donatedAt": "2018-08-20T06:00:18Z",
    "donor": {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "anonymous": true,
      "businessName": "string",
      "donorId": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "newsletter": true,
      "phoneNumber": "string"
    },
    "financials": {
      "cardBrand": "string",
      "cardCountry": "string",
      "cardLast4Digits": "string",
      "currency": "string",
      "fee": 0,
      "feeCovered": true,
      "platform": "stripe",
      "refunded": true,
      "refundedAt": "2018-08-20T06:00:18Z",
      "refundedAtLocal": "2018-08-20T06:00:18Z",
      "subscription": true,
      "tax": 0,
      "totalFees": 0,
      "timezone": "string"
    },
    "fundraiserId": 0,
    "fundraiser": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAt": "2018-08-20T06:00:18Z",
    "message": "string",
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "pageType": "campaign",
    "receiptNumber": "string",
    "reply": {
      "displayFirstName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "repliedAtLocal": "2018-08-20T06:00:18Z",
      "repliedAt": "2018-08-20T06:00:18Z",
      "reply": "string"
    },
    "status": "collectedFromCustomer",
    "teamId": 0,
    "team": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "type": "online"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accesskeypost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccessKeySearchPost

<a id="opIdApiV2AccessKeySearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/AccessKey/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/AccessKey/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/AccessKey/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/AccessKey/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/AccessKey/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/AccessKey/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/AccessKey/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/AccessKey/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/AccessKey/search`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2accesskeysearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccessKeySearchModel](#schemaaccesskeysearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "organizationId": 0,
        "organization": {
          "id": 0,
          "name": "string",
          "urlPath": "string"
        },
        "clientKey": "string",
        "description": "string",
        "createdAt": "2018-08-20T06:00:18Z"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accesskeysearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_AccessKeyElementModel_](#schemalistactionresult_accesskeyelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_AccessKeyElementModel_](#schemalistactionresult_accesskeyelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccessKeyExportPost

<a id="opIdApiV2AccessKeyExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/AccessKey/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/AccessKey/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/AccessKey/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/AccessKey/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/AccessKey/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/AccessKey/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/AccessKey/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/AccessKey/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/AccessKey/export`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2accesskeyexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccessKeySearchModel](#schemaaccesskeysearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accesskeyexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccessKeyMetadataGet

<a id="opIdApiV2AccessKeyMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/AccessKey/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/AccessKey/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/AccessKey/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/AccessKey/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/AccessKey/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/AccessKey/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/AccessKey/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/AccessKey/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/AccessKey/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accesskeymetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-Account">Account</h1>

## ApiV2AccountByIdGet

<a id="opIdApiV2AccountByIdGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Account/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Account/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Account/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Account/{id}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Account/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Account/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Account/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Account/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Account/{id}`

*Gets an acccount object by id*

<h3 id="apiv2accountbyidget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Account id|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 0,
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "createdAt": "2018-08-20T06:00:18Z",
    "lastLoggedInAt": "2018-08-20T06:00:18Z",
    "status": "active",
    "roles": "notDefined",
    "isOrgAdmin": true,
    "isSysAdmin": true,
    "isFundraiser": true,
    "isAdmin": true,
    "organizationId": 0,
    "source": "default",
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountbyidget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_AccountElementModel_](#schemascalaractionresult_accountelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_AccountElementModel_](#schemascalaractionresult_accountelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountByIdPut

<a id="opIdApiV2AccountByIdPut"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT //api.dev.grassrootz.com//api/v2/Account/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PUT //api.dev.grassrootz.com//api/v2/Account/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Account/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "password": "string",
  "mainImagePath": "string",
  "organizationId": 0,
  "roles": "notDefined",
  "asInvite": true,
  "asPublicJoin": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Account/{id}',
{
  method: 'PUT',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.put '//api.dev.grassrootz.com//api/v2/Account/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.put('//api.dev.grassrootz.com//api/v2/Account/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Account/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "//api.dev.grassrootz.com//api/v2/Account/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v2/Account/{id}`

*Updates an account object by id*

> Body parameter

```json
{
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "password": "string",
  "mainImagePath": "string",
  "organizationId": 0,
  "roles": "notDefined",
  "asInvite": true,
  "asPublicJoin": true
}
```

<h3 id="apiv2accountbyidput-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the account object being modified|
|body|body|[AccountEditModel](#schemaaccounteditmodel)|false|The account model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 0,
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "createdAt": "2018-08-20T06:00:18Z",
    "lastLoggedInAt": "2018-08-20T06:00:18Z",
    "status": "active",
    "roles": "notDefined",
    "isOrgAdmin": true,
    "isSysAdmin": true,
    "isFundraiser": true,
    "isAdmin": true,
    "organizationId": 0,
    "source": "default",
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountbyidput-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_AccountElementModel_](#schemascalaractionresult_accountelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_AccountElementModel_](#schemascalaractionresult_accountelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountByIdDelete

<a id="opIdApiV2AccountByIdDelete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE //api.dev.grassrootz.com//api/v2/Account/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
DELETE //api.dev.grassrootz.com//api/v2/Account/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Account/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Account/{id}',
{
  method: 'DELETE',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.delete '//api.dev.grassrootz.com//api/v2/Account/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.delete('//api.dev.grassrootz.com//api/v2/Account/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Account/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "//api.dev.grassrootz.com//api/v2/Account/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/Account/{id}`

*Patches (partial update) an account object by id*

<h3 id="apiv2accountbyiddelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the account object being modified|

> Example responses

> 200 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountbyiddelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountByIdPatch

<a id="opIdApiV2AccountByIdPatch"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH //api.dev.grassrootz.com//api/v2/Account/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PATCH //api.dev.grassrootz.com//api/v2/Account/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Account/{id}',
  method: 'patch',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Account/{id}',
{
  method: 'PATCH',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.patch '//api.dev.grassrootz.com//api/v2/Account/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.patch('//api.dev.grassrootz.com//api/v2/Account/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Account/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "//api.dev.grassrootz.com//api/v2/Account/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v2/Account/{id}`

*Patches (partial update) an account object by id*

> Body parameter

```json
[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]
```

<h3 id="apiv2accountbyidpatch-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the account object being modified|
|body|body|array[object]|false|The account model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 0,
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "createdAt": "2018-08-20T06:00:18Z",
    "lastLoggedInAt": "2018-08-20T06:00:18Z",
    "status": "active",
    "roles": "notDefined",
    "isOrgAdmin": true,
    "isSysAdmin": true,
    "isFundraiser": true,
    "isAdmin": true,
    "organizationId": 0,
    "source": "default",
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountbyidpatch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_AccountElementModel_](#schemascalaractionresult_accountelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_AccountElementModel_](#schemascalaractionresult_accountelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountPost

<a id="opIdApiV2AccountPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Account \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Account HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Account',
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
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "password": "string",
  "mainImagePath": "string",
  "organizationId": 0,
  "roles": "notDefined",
  "asInvite": true,
  "asPublicJoin": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Account',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Account',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Account', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Account");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Account", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Account`

*Creates a new account*

> Body parameter

```json
{
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "password": "string",
  "mainImagePath": "string",
  "organizationId": 0,
  "roles": "notDefined",
  "asInvite": true,
  "asPublicJoin": true
}
```

<h3 id="apiv2accountpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccountEditModel](#schemaaccounteditmodel)|false|The account model containing the details|

> Example responses

> 201 Response

```json
{
  "data": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "sessionKey": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_AccountPublicModel_](#schemascalaractionresult_accountpublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_AccountPublicModel_](#schemascalaractionresult_accountpublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2AccountPasswordResetPost

<a id="opIdApiV2AccountPasswordResetPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Account/password/reset \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Account/password/reset HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Account/password/reset',
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
  "email": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Account/password/reset',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Account/password/reset',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Account/password/reset', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Account/password/reset");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Account/password/reset", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Account/password/reset`

*Starts a password reset process*

> Body parameter

```json
{
  "email": "string"
}
```

<h3 id="apiv2accountpasswordresetpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccountPasswordResetRequestModel](#schemaaccountpasswordresetrequestmodel)|false|The model containing the account to be used for the operation|

> Example responses

> 201 Response

```json
{
  "data": "string",
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountpasswordresetpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_String_](#schemascalaractionresult_string_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_String_](#schemascalaractionresult_string_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2AccountPasswordUpdatePost

<a id="opIdApiV2AccountPasswordUpdatePost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Account/password/update \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Account/password/update HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Account/password/update',
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
  "token": "string",
  "newPassword": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Account/password/update',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Account/password/update',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Account/password/update', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Account/password/update");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Account/password/update", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Account/password/update`

*Updates the password for a specific account based on an email and reset token*

> Body parameter

```json
{
  "token": "string",
  "newPassword": "string"
}
```

<h3 id="apiv2accountpasswordupdatepost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccountPasswordResetModel](#schemaaccountpasswordresetmodel)|false|The model containing the account to be used for the operation|

> Example responses

> 201 Response

```json
{
  "data": "string",
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountpasswordupdatepost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_String_](#schemascalaractionresult_string_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_String_](#schemascalaractionresult_string_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2AccountSearchPost

<a id="opIdApiV2AccountSearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Account/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Account/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Account/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Account/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Account/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Account/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Account/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Account/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Account/search`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2accountsearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccountSearchModel](#schemaaccountsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "id": 0,
        "email": "string",
        "firstName": "string",
        "lastName": "string",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "createdAt": "2018-08-20T06:00:18Z",
        "lastLoggedInAt": "2018-08-20T06:00:18Z",
        "status": "active",
        "roles": "notDefined",
        "isOrgAdmin": true,
        "isSysAdmin": true,
        "isFundraiser": true,
        "isAdmin": true,
        "organizationId": 0,
        "source": "default",
        "organization": {
          "id": 0,
          "name": "string",
          "urlPath": "string"
        }
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountsearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_AccountElementModel_](#schemalistactionresult_accountelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_AccountElementModel_](#schemalistactionresult_accountelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountExportPost

<a id="opIdApiV2AccountExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Account/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Account/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Account/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Account/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Account/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Account/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Account/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Account/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Account/export`

*Search (List request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2accountexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccountSearchModel](#schemaaccountsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountMetadataGet

<a id="opIdApiV2AccountMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Account/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Account/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Account/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Account/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Account/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Account/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Account/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Account/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Account/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountmetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountAggregateGet

<a id="opIdApiV2AccountAggregateGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Account/aggregate \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Account/aggregate HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Account/aggregate',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Account/aggregate',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Account/aggregate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Account/aggregate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Account/aggregate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Account/aggregate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Account/aggregate`

*Perform an aggregate function on a field based on a filter/custom-text criteria*

<h3 id="apiv2accountaggregateget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|fieldName|query|string|false|none|
|fieldAggregate|query|string|false|none|
|filters|query|array[any]|false|none|
|text|query|string|false|none|
|orderBy.key|query|string|false|none|
|orderBy.direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|pageSize|query|integer(int32)|false|none|
|resultType|query|string|false|none|
|includeDataTemplate|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|fieldAggregate|sum|
|fieldAggregate|average|
|fieldAggregate|min|
|fieldAggregate|max|
|fieldAggregate|count|
|orderBy.direction|asc|
|orderBy.direction|desc|
|resultType|lookup|
|resultType|basic|
|resultType|full|

> Example responses

> 200 Response

```json
{
  "data": 0,
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountaggregateget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-AccountDonor">AccountDonor</h1>

## ApiV2AccountDonorSearchPost

<a id="opIdApiV2AccountDonorSearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/account/donor/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/account/donor/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/account/donor/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/account/donor/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/account/donor/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/account/donor/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/account/donor/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/account/donor/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/account/donor/search`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2accountdonorsearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccountDonorSearchModel](#schemaaccountdonorsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "id": 0,
        "email": "string",
        "firstName": "string",
        "lastName": "string",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "createdAt": "2018-08-20T06:00:18Z",
        "donationCount": 0,
        "raisedAmount": 0,
        "averageDonationAmount": 0
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountdonorsearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_AccountDonorElementModel_](#schemalistactionresult_accountdonorelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_AccountDonorElementModel_](#schemalistactionresult_accountdonorelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountDonorExportPost

<a id="opIdApiV2AccountDonorExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/account/donor/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/account/donor/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/account/donor/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/account/donor/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/account/donor/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/account/donor/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/account/donor/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/account/donor/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/account/donor/export`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2accountdonorexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccountDonorSearchModel](#schemaaccountdonorsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountdonorexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountDonorMetadataGet

<a id="opIdApiV2AccountDonorMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/account/donor/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/account/donor/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/account/donor/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/account/donor/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/account/donor/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/account/donor/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/account/donor/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/account/donor/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/account/donor/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountdonormetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountDonorAggregateGet

<a id="opIdApiV2AccountDonorAggregateGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/account/donor/aggregate \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/account/donor/aggregate HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/account/donor/aggregate',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/account/donor/aggregate',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/account/donor/aggregate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/account/donor/aggregate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/account/donor/aggregate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/account/donor/aggregate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/account/donor/aggregate`

*Perform an aggregate function on a field based on a filter/custom-text criteria*

<h3 id="apiv2accountdonoraggregateget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|fieldName|query|string|false|none|
|fieldAggregate|query|string|false|none|
|filters|query|array[any]|false|none|
|text|query|string|false|none|
|orderBy.key|query|string|false|none|
|orderBy.direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|pageSize|query|integer(int32)|false|none|
|resultType|query|string|false|none|
|includeDataTemplate|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|fieldAggregate|sum|
|fieldAggregate|average|
|fieldAggregate|min|
|fieldAggregate|max|
|fieldAggregate|count|
|orderBy.direction|asc|
|orderBy.direction|desc|
|resultType|lookup|
|resultType|basic|
|resultType|full|

> Example responses

> 200 Response

```json
{
  "data": 0,
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountdonoraggregateget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-AccountFundraiser">AccountFundraiser</h1>

## ApiV2AccountFundraiserSearchPost

<a id="opIdApiV2AccountFundraiserSearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/account/fundraiser/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/account/fundraiser/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/account/fundraiser/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/account/fundraiser/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/account/fundraiser/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/account/fundraiser/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/account/fundraiser/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/account/fundraiser/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/account/fundraiser/search`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2accountfundraisersearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccountFundraiserSearchModel](#schemaaccountfundraisersearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "id": 0,
        "email": "string",
        "firstName": "string",
        "lastName": "string",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "createdAt": "2018-08-20T06:00:18Z",
        "donationCount": 0,
        "raisedAmount": 0,
        "averageDonationAmount": 0,
        "activePagesCount": 0,
        "pagesCount": 0
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountfundraisersearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_AccountFundraiserElementModel_](#schemalistactionresult_accountfundraiserelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_AccountFundraiserElementModel_](#schemalistactionresult_accountfundraiserelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountFundraiserExportPost

<a id="opIdApiV2AccountFundraiserExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/account/fundraiser/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/account/fundraiser/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/account/fundraiser/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/account/fundraiser/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/account/fundraiser/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/account/fundraiser/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/account/fundraiser/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/account/fundraiser/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/account/fundraiser/export`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2accountfundraiserexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AccountFundraiserSearchModel](#schemaaccountfundraisersearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountfundraiserexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountFundraiserMetadataGet

<a id="opIdApiV2AccountFundraiserMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/account/fundraiser/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/account/fundraiser/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/account/fundraiser/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/account/fundraiser/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/account/fundraiser/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/account/fundraiser/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/account/fundraiser/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/account/fundraiser/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/account/fundraiser/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountfundraisermetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2AccountFundraiserAggregateGet

<a id="opIdApiV2AccountFundraiserAggregateGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/account/fundraiser/aggregate \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/account/fundraiser/aggregate HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/account/fundraiser/aggregate',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/account/fundraiser/aggregate',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/account/fundraiser/aggregate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/account/fundraiser/aggregate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/account/fundraiser/aggregate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/account/fundraiser/aggregate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/account/fundraiser/aggregate`

*Perform an aggregate function on a field based on a filter/custom-text criteria*

<h3 id="apiv2accountfundraiseraggregateget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|fieldName|query|string|false|none|
|fieldAggregate|query|string|false|none|
|filters|query|array[any]|false|none|
|text|query|string|false|none|
|orderBy.key|query|string|false|none|
|orderBy.direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|pageSize|query|integer(int32)|false|none|
|resultType|query|string|false|none|
|includeDataTemplate|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|fieldAggregate|sum|
|fieldAggregate|average|
|fieldAggregate|min|
|fieldAggregate|max|
|fieldAggregate|count|
|orderBy.direction|asc|
|orderBy.direction|desc|
|resultType|lookup|
|resultType|basic|
|resultType|full|

> Example responses

> 200 Response

```json
{
  "data": 0,
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2accountfundraiseraggregateget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-Campaign">Campaign</h1>

## ApiV2PageCampaignByIdGet

<a id="opIdApiV2PageCampaignByIdGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Campaign/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Campaign/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Campaign/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Campaign/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Campaign/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Campaign/{id}`

*Gets a campaign object by id*

<h3 id="apiv2pagecampaignbyidget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Campaign id|

> Example responses

> 200 Response

```json
{
  "data": {
    "activePagesCount": 0,
    "additionalDonationsNeededForTarget": 0,
    "averageDonationAmount": 0,
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "dataCapture": {
      "registration": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      },
      "donation": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      }
    },
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "fundraisersActiveCount": 0,
    "fundraisersCount": 0,
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAtUtc": "2018-08-20T06:00:18Z",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organizationId": 0,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "organizationPaymentPlatformId": 0,
    "pagesCount": 0,
    "paymentPlatforms": {
      "main": {
        "id": 0,
        "platform": "stripe",
        "platformType": "creditCardForm",
        "publicKey": "string"
      },
      "alternative": [
        {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        }
      ]
    },
    "raisedAmount": 0,
    "targetAmount": 0,
    "type": "default",
    "status": "live",
    "teamsActiveCount": 0,
    "teamsCount": 0,
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagecampaignbyidget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_CampaignElementModel_](#schemascalaractionresult_campaignelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_CampaignElementModel_](#schemascalaractionresult_campaignelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageCampaignByIdPut

<a id="opIdApiV2PageCampaignByIdPut"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT //api.dev.grassrootz.com//api/v2/page/Campaign/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PUT //api.dev.grassrootz.com//api/v2/page/Campaign/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "fields": {
    "Registration": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Donation": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Ticket": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ]
  },
  "status": "live",
  "targetAmount": 0,
  "organizationId": 0,
  "eventId": 0,
  "organizationPaymentPlatformId": 0,
  "name": "string",
  "mainImagePath": "string",
  "urlPath": "string",
  "type": "default",
  "dataCapture": {
    "registration": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    },
    "donation": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    }
  },
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "template": {
    "key": "string",
    "value": {}
  },
  "additionalPaymentPlatformIds": [
    0
  ]
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
{
  method: 'PUT',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.put '//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.put('//api.dev.grassrootz.com//api/v2/page/Campaign/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Campaign/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "//api.dev.grassrootz.com//api/v2/page/Campaign/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v2/page/Campaign/{id}`

*Updates a campaign object by id*

> Body parameter

```json
{
  "fields": {
    "Registration": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Donation": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Ticket": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ]
  },
  "status": "live",
  "targetAmount": 0,
  "organizationId": 0,
  "eventId": 0,
  "organizationPaymentPlatformId": 0,
  "name": "string",
  "mainImagePath": "string",
  "urlPath": "string",
  "type": "default",
  "dataCapture": {
    "registration": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    },
    "donation": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    }
  },
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "template": {
    "key": "string",
    "value": {}
  },
  "additionalPaymentPlatformIds": [
    0
  ]
}
```

<h3 id="apiv2pagecampaignbyidput-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the campaign object being modified|
|body|body|[CampaignEditModel](#schemacampaigneditmodel)|false|The campaign model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "activePagesCount": 0,
    "additionalDonationsNeededForTarget": 0,
    "averageDonationAmount": 0,
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "dataCapture": {
      "registration": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      },
      "donation": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      }
    },
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "fundraisersActiveCount": 0,
    "fundraisersCount": 0,
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAtUtc": "2018-08-20T06:00:18Z",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organizationId": 0,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "organizationPaymentPlatformId": 0,
    "pagesCount": 0,
    "paymentPlatforms": {
      "main": {
        "id": 0,
        "platform": "stripe",
        "platformType": "creditCardForm",
        "publicKey": "string"
      },
      "alternative": [
        {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        }
      ]
    },
    "raisedAmount": 0,
    "targetAmount": 0,
    "type": "default",
    "status": "live",
    "teamsActiveCount": 0,
    "teamsCount": 0,
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagecampaignbyidput-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_CampaignElementModel_](#schemascalaractionresult_campaignelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_CampaignElementModel_](#schemascalaractionresult_campaignelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageCampaignByIdDelete

<a id="opIdApiV2PageCampaignByIdDelete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE //api.dev.grassrootz.com//api/v2/page/Campaign/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
DELETE //api.dev.grassrootz.com//api/v2/page/Campaign/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
{
  method: 'DELETE',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.delete '//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.delete('//api.dev.grassrootz.com//api/v2/page/Campaign/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Campaign/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "//api.dev.grassrootz.com//api/v2/page/Campaign/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/page/Campaign/{id}`

*Patches (partial update) a campaign object by id*

<h3 id="apiv2pagecampaignbyiddelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the campaign object being modified|

> Example responses

> 200 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagecampaignbyiddelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageCampaignByIdPatch

<a id="opIdApiV2PageCampaignByIdPatch"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH //api.dev.grassrootz.com//api/v2/page/Campaign/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PATCH //api.dev.grassrootz.com//api/v2/page/Campaign/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
  method: 'patch',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
{
  method: 'PATCH',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.patch '//api.dev.grassrootz.com//api/v2/page/Campaign/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.patch('//api.dev.grassrootz.com//api/v2/page/Campaign/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Campaign/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "//api.dev.grassrootz.com//api/v2/page/Campaign/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v2/page/Campaign/{id}`

*Patches (partial update) a campaign object by id*

> Body parameter

```json
[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]
```

<h3 id="apiv2pagecampaignbyidpatch-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the campaign object being modified|
|body|body|array[object]|false|The campaign model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "activePagesCount": 0,
    "additionalDonationsNeededForTarget": 0,
    "averageDonationAmount": 0,
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "dataCapture": {
      "registration": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      },
      "donation": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      }
    },
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "fundraisersActiveCount": 0,
    "fundraisersCount": 0,
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAtUtc": "2018-08-20T06:00:18Z",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organizationId": 0,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "organizationPaymentPlatformId": 0,
    "pagesCount": 0,
    "paymentPlatforms": {
      "main": {
        "id": 0,
        "platform": "stripe",
        "platformType": "creditCardForm",
        "publicKey": "string"
      },
      "alternative": [
        {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        }
      ]
    },
    "raisedAmount": 0,
    "targetAmount": 0,
    "type": "default",
    "status": "live",
    "teamsActiveCount": 0,
    "teamsCount": 0,
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagecampaignbyidpatch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_CampaignElementModel_](#schemascalaractionresult_campaignelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_CampaignElementModel_](#schemascalaractionresult_campaignelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageCampaignPublicByPrimaryPathBySecondaryPathGet

<a id="opIdApiV2PageCampaignPublicByPrimaryPathBySecondaryPathGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Campaign/public/{primaryPath}/{secondaryPath} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Campaign/public/{primaryPath}/{secondaryPath} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Campaign/public/{primaryPath}/{secondaryPath}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Campaign/public/{primaryPath}/{secondaryPath}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Campaign/public/{primaryPath}/{secondaryPath}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Campaign/public/{primaryPath}/{secondaryPath}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Campaign/public/{primaryPath}/{secondaryPath}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Campaign/public/{primaryPath}/{secondaryPath}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Campaign/public/{primaryPath}/{secondaryPath}`

*Gets a campaign object by paths*

<h3 id="apiv2pagecampaignpublicbyprimarypathbysecondarypathget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|primaryPath|path|string|true|Organization/Event Url Path|
|secondaryPath|path|string|true|Campaign/Org Url Path|

> Example responses

> 200 Response

```json
{
  "data": {
    "additionalDonationsNeededForTarget": 0,
    "averageDonationAmount": 0,
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "dataCapture": {
      "registration": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      },
      "donation": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      }
    },
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "fundraisersCount": 0,
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organizationId": 0,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "pagesCount": 0,
    "paymentPlatforms": {
      "main": {
        "id": 0,
        "platform": "stripe",
        "platformType": "creditCardForm",
        "publicKey": "string"
      },
      "alternative": [
        {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        }
      ]
    },
    "raisedAmount": 0,
    "targetAmount": 0,
    "type": "default",
    "status": "live",
    "teamsCount": 0,
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagecampaignpublicbyprimarypathbysecondarypathget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_CampaignPublicModel_](#schemascalaractionresult_campaignpublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_CampaignPublicModel_](#schemascalaractionresult_campaignpublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2PageCampaignPost

<a id="opIdApiV2PageCampaignPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Campaign \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Campaign HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Campaign',
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
  "fields": {
    "Registration": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Donation": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Ticket": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ]
  },
  "status": "live",
  "targetAmount": 0,
  "organizationId": 0,
  "eventId": 0,
  "organizationPaymentPlatformId": 0,
  "name": "string",
  "mainImagePath": "string",
  "urlPath": "string",
  "type": "default",
  "dataCapture": {
    "registration": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    },
    "donation": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    }
  },
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "template": {
    "key": "string",
    "value": {}
  },
  "additionalPaymentPlatformIds": [
    0
  ]
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Campaign',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Campaign',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Campaign', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Campaign");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Campaign", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Campaign`

*Creates a new campaign*

> Body parameter

```json
{
  "fields": {
    "Registration": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Donation": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Ticket": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ]
  },
  "status": "live",
  "targetAmount": 0,
  "organizationId": 0,
  "eventId": 0,
  "organizationPaymentPlatformId": 0,
  "name": "string",
  "mainImagePath": "string",
  "urlPath": "string",
  "type": "default",
  "dataCapture": {
    "registration": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    },
    "donation": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    }
  },
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "template": {
    "key": "string",
    "value": {}
  },
  "additionalPaymentPlatformIds": [
    0
  ]
}
```

<h3 id="apiv2pagecampaignpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CampaignEditModel](#schemacampaigneditmodel)|false|The campaign model containing the details|

> Example responses

> 201 Response

```json
{
  "data": {
    "activePagesCount": 0,
    "additionalDonationsNeededForTarget": 0,
    "averageDonationAmount": 0,
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "dataCapture": {
      "registration": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      },
      "donation": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      }
    },
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "fundraisersActiveCount": 0,
    "fundraisersCount": 0,
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAtUtc": "2018-08-20T06:00:18Z",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organizationId": 0,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "organizationPaymentPlatformId": 0,
    "pagesCount": 0,
    "paymentPlatforms": {
      "main": {
        "id": 0,
        "platform": "stripe",
        "platformType": "creditCardForm",
        "publicKey": "string"
      },
      "alternative": [
        {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        }
      ]
    },
    "raisedAmount": 0,
    "targetAmount": 0,
    "type": "default",
    "status": "live",
    "teamsActiveCount": 0,
    "teamsCount": 0,
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagecampaignpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_CampaignElementModel_](#schemascalaractionresult_campaignelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_CampaignElementModel_](#schemascalaractionresult_campaignelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageCampaignSearchPost

<a id="opIdApiV2PageCampaignSearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Campaign/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Campaign/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Campaign/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Campaign/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Campaign/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Campaign/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Campaign/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Campaign/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Campaign/search`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2pagecampaignsearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CampaignSearchModel](#schemacampaignsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "activePagesCount": 0,
        "additionalDonationsNeededForTarget": 0,
        "averageDonationAmount": 0,
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "dataCapture": {
          "registration": {
            "phone": {
              "capture": true,
              "mandatory": true
            },
            "address": {
              "capture": true,
              "mandatory": true
            }
          },
          "donation": {
            "phone": {
              "capture": true,
              "mandatory": true
            },
            "address": {
              "capture": true,
              "mandatory": true
            }
          }
        },
        "donationCount": 0,
        "donationSetup": {
          "allowRecurringGiving": true
        },
        "fundraisersActiveCount": 0,
        "fundraisersCount": 0,
        "fundraisers": {
          "enabled": true,
          "defaultTargetAmount": 0,
          "allowSelfSignUp": true
        },
        "id": 0,
        "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
        "lastUpdatedAtUtc": "2018-08-20T06:00:18Z",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "organizationId": 0,
        "organization": {
          "country": "string",
          "currency": "string",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "organizationPaymentPlatformId": 0,
        "pagesCount": 0,
        "paymentPlatforms": {
          "main": {
            "id": 0,
            "platform": "stripe",
            "platformType": "creditCardForm",
            "publicKey": "string"
          },
          "alternative": [
            {
              "id": 0,
              "platform": "stripe",
              "platformType": "creditCardForm",
              "publicKey": "string"
            }
          ]
        },
        "raisedAmount": 0,
        "targetAmount": 0,
        "type": "default",
        "status": "live",
        "teamsActiveCount": 0,
        "teamsCount": 0,
        "teams": {
          "enabled": true,
          "defaultTargetAmount": 0,
          "allowSelfSignUp": true
        },
        "template": {
          "key": "string",
          "value": {}
        },
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagecampaignsearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_CampaignElementModel_](#schemalistactionresult_campaignelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_CampaignElementModel_](#schemalistactionresult_campaignelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageCampaignExportPost

<a id="opIdApiV2PageCampaignExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Campaign/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Campaign/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Campaign/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Campaign/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Campaign/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Campaign/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Campaign/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Campaign/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Campaign/export`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2pagecampaignexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[CampaignSearchModel](#schemacampaignsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagecampaignexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageCampaignMetadataGet

<a id="opIdApiV2PageCampaignMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Campaign/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Campaign/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Campaign/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Campaign/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Campaign/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Campaign/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Campaign/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Campaign/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Campaign/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagecampaignmetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageCampaignAggregateGet

<a id="opIdApiV2PageCampaignAggregateGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Campaign/aggregate \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Campaign/aggregate HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Campaign/aggregate',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Campaign/aggregate',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Campaign/aggregate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Campaign/aggregate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Campaign/aggregate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Campaign/aggregate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Campaign/aggregate`

*Perform an aggregate function on a field based on a filter/custom-text criteria*

<h3 id="apiv2pagecampaignaggregateget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|fieldName|query|string|false|none|
|fieldAggregate|query|string|false|none|
|filters|query|array[any]|false|none|
|text|query|string|false|none|
|orderBy.key|query|string|false|none|
|orderBy.direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|pageSize|query|integer(int32)|false|none|
|resultType|query|string|false|none|
|includeDataTemplate|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|fieldAggregate|sum|
|fieldAggregate|average|
|fieldAggregate|min|
|fieldAggregate|max|
|fieldAggregate|count|
|orderBy.direction|asc|
|orderBy.direction|desc|
|resultType|lookup|
|resultType|basic|
|resultType|full|

> Example responses

> 200 Response

```json
{
  "data": 0,
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagecampaignaggregateget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-Donation">Donation</h1>

## ApiV2DonationByIdGet

<a id="opIdApiV2DonationByIdGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Donation/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Donation/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/{id}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Donation/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Donation/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Donation/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Donation/{id}`

*Gets a donation object by id*

<h3 id="apiv2donationbyidget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Donation id|

> Example responses

> 200 Response

```json
{
  "data": {
    "accountId": 0,
    "amount": 0,
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string",
      "template": {
        "key": "string",
        "value": {}
      }
    },
    "donatedAtLocal": "2018-08-20T06:00:18Z",
    "donatedAt": "2018-08-20T06:00:18Z",
    "donor": {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "anonymous": true,
      "businessName": "string",
      "donorId": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "newsletter": true,
      "phoneNumber": "string"
    },
    "financials": {
      "cardBrand": "string",
      "cardCountry": "string",
      "cardLast4Digits": "string",
      "currency": "string",
      "fee": 0,
      "feeCovered": true,
      "platform": "stripe",
      "refunded": true,
      "refundedAt": "2018-08-20T06:00:18Z",
      "refundedAtLocal": "2018-08-20T06:00:18Z",
      "subscription": true,
      "tax": 0,
      "totalFees": 0,
      "timezone": "string"
    },
    "fundraiserId": 0,
    "fundraiser": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAt": "2018-08-20T06:00:18Z",
    "message": "string",
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "pageType": "campaign",
    "receiptNumber": "string",
    "reply": {
      "displayFirstName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "repliedAtLocal": "2018-08-20T06:00:18Z",
      "repliedAt": "2018-08-20T06:00:18Z",
      "reply": "string"
    },
    "status": "collectedFromCustomer",
    "teamId": 0,
    "team": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "type": "online"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationbyidget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationByIdPut

<a id="opIdApiV2DonationByIdPut"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT //api.dev.grassrootz.com//api/v2/Donation/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PUT //api.dev.grassrootz.com//api/v2/Donation/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "amount": 0,
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "customer": {
    "anonymous": true,
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "businessName": "string",
    "email": "string",
    "firstName": "string",
    "fromCredential": true,
    "lastName": "string",
    "newsletter": true,
    "phoneNumber": "string"
  },
  "fundraiserId": 0,
  "issueReceipt": true,
  "message": "string",
  "payment": {
    "cardBrand": "string",
    "cardCountry": "string",
    "cardExpiryMonth": 0,
    "cardExpiryYear": 0,
    "cardLast4Digits": "stri",
    "coverFee": true,
    "token": "string"
  },
  "teamId": 0,
  "pageType": "campaign",
  "template": {
    "key": "string",
    "value": {}
  },
  "type": "online"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/{id}',
{
  method: 'PUT',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.put '//api.dev.grassrootz.com//api/v2/Donation/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.put('//api.dev.grassrootz.com//api/v2/Donation/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "//api.dev.grassrootz.com//api/v2/Donation/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v2/Donation/{id}`

*Updates a donation object by id*

> Body parameter

```json
{
  "amount": 0,
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "customer": {
    "anonymous": true,
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "businessName": "string",
    "email": "string",
    "firstName": "string",
    "fromCredential": true,
    "lastName": "string",
    "newsletter": true,
    "phoneNumber": "string"
  },
  "fundraiserId": 0,
  "issueReceipt": true,
  "message": "string",
  "payment": {
    "cardBrand": "string",
    "cardCountry": "string",
    "cardExpiryMonth": 0,
    "cardExpiryYear": 0,
    "cardLast4Digits": "stri",
    "coverFee": true,
    "token": "string"
  },
  "teamId": 0,
  "pageType": "campaign",
  "template": {
    "key": "string",
    "value": {}
  },
  "type": "online"
}
```

<h3 id="apiv2donationbyidput-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the donation object being modified|
|body|body|[DonationEditModel](#schemadonationeditmodel)|false|The donation model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "accountId": 0,
    "amount": 0,
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string",
      "template": {
        "key": "string",
        "value": {}
      }
    },
    "donatedAtLocal": "2018-08-20T06:00:18Z",
    "donatedAt": "2018-08-20T06:00:18Z",
    "donor": {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "anonymous": true,
      "businessName": "string",
      "donorId": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "newsletter": true,
      "phoneNumber": "string"
    },
    "financials": {
      "cardBrand": "string",
      "cardCountry": "string",
      "cardLast4Digits": "string",
      "currency": "string",
      "fee": 0,
      "feeCovered": true,
      "platform": "stripe",
      "refunded": true,
      "refundedAt": "2018-08-20T06:00:18Z",
      "refundedAtLocal": "2018-08-20T06:00:18Z",
      "subscription": true,
      "tax": 0,
      "totalFees": 0,
      "timezone": "string"
    },
    "fundraiserId": 0,
    "fundraiser": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAt": "2018-08-20T06:00:18Z",
    "message": "string",
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "pageType": "campaign",
    "receiptNumber": "string",
    "reply": {
      "displayFirstName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "repliedAtLocal": "2018-08-20T06:00:18Z",
      "repliedAt": "2018-08-20T06:00:18Z",
      "reply": "string"
    },
    "status": "collectedFromCustomer",
    "teamId": 0,
    "team": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "type": "online"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationbyidput-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationByIdDelete

<a id="opIdApiV2DonationByIdDelete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE //api.dev.grassrootz.com//api/v2/Donation/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
DELETE //api.dev.grassrootz.com//api/v2/Donation/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/{id}',
{
  method: 'DELETE',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.delete '//api.dev.grassrootz.com//api/v2/Donation/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.delete('//api.dev.grassrootz.com//api/v2/Donation/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "//api.dev.grassrootz.com//api/v2/Donation/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/Donation/{id}`

*Patches (partial update) a donation object by id*

<h3 id="apiv2donationbyiddelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the donation object being modified|

> Example responses

> 200 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationbyiddelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationByIdPatch

<a id="opIdApiV2DonationByIdPatch"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH //api.dev.grassrootz.com//api/v2/Donation/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PATCH //api.dev.grassrootz.com//api/v2/Donation/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/{id}',
  method: 'patch',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/{id}',
{
  method: 'PATCH',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.patch '//api.dev.grassrootz.com//api/v2/Donation/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.patch('//api.dev.grassrootz.com//api/v2/Donation/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "//api.dev.grassrootz.com//api/v2/Donation/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v2/Donation/{id}`

*Patches (partial update) a donation object by id*

> Body parameter

```json
[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]
```

<h3 id="apiv2donationbyidpatch-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the donation object being modified|
|body|body|[OperationArray](#schemaoperationarray)|false|The donation model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "accountId": 0,
    "amount": 0,
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string",
      "template": {
        "key": "string",
        "value": {}
      }
    },
    "donatedAtLocal": "2018-08-20T06:00:18Z",
    "donatedAt": "2018-08-20T06:00:18Z",
    "donor": {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "anonymous": true,
      "businessName": "string",
      "donorId": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "newsletter": true,
      "phoneNumber": "string"
    },
    "financials": {
      "cardBrand": "string",
      "cardCountry": "string",
      "cardLast4Digits": "string",
      "currency": "string",
      "fee": 0,
      "feeCovered": true,
      "platform": "stripe",
      "refunded": true,
      "refundedAt": "2018-08-20T06:00:18Z",
      "refundedAtLocal": "2018-08-20T06:00:18Z",
      "subscription": true,
      "tax": 0,
      "totalFees": 0,
      "timezone": "string"
    },
    "fundraiserId": 0,
    "fundraiser": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAt": "2018-08-20T06:00:18Z",
    "message": "string",
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "pageType": "campaign",
    "receiptNumber": "string",
    "reply": {
      "displayFirstName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "repliedAtLocal": "2018-08-20T06:00:18Z",
      "repliedAt": "2018-08-20T06:00:18Z",
      "reply": "string"
    },
    "status": "collectedFromCustomer",
    "teamId": 0,
    "team": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "type": "online"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationbyidpatch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationFeeByPrimaryPathBySecondaryPathGet

<a id="opIdApiV2DonationFeeByPrimaryPathBySecondaryPathGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Donation/fee/{primaryPath}/{secondaryPath} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Donation/fee/{primaryPath}/{secondaryPath} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/fee/{primaryPath}/{secondaryPath}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/fee/{primaryPath}/{secondaryPath}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Donation/fee/{primaryPath}/{secondaryPath}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Donation/fee/{primaryPath}/{secondaryPath}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/fee/{primaryPath}/{secondaryPath}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Donation/fee/{primaryPath}/{secondaryPath}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Donation/fee/{primaryPath}/{secondaryPath}`

*Gets a donation object by id*

<h3 id="apiv2donationfeebyprimarypathbysecondarypathget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|amount|query|number(double)|false|The amount to be donated|
|coverFee|query|boolean|false|Whether the person will cover the platform fee|
|primaryPath|path|string|true|Organization/Event Url Path|
|secondaryPath|path|string|true|Campaign/Org Url Path|

> Example responses

> 200 Response

```json
{
  "data": {
    "amount": 0,
    "fee": 0,
    "tax": 0,
    "totalFees": 0,
    "totalWithFees": 0
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationfeebyprimarypathbysecondarypathget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_DonationFeeCalculationElementModel_](#schemascalaractionresult_donationfeecalculationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_DonationFeeCalculationElementModel_](#schemascalaractionresult_donationfeecalculationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2DonationPost

<a id="opIdApiV2DonationPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Donation \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Donation HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation',
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
  "amount": 0,
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "customer": {
    "anonymous": true,
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "businessName": "string",
    "email": "string",
    "firstName": "string",
    "fromCredential": true,
    "lastName": "string",
    "newsletter": true,
    "phoneNumber": "string"
  },
  "fundraiserId": 0,
  "issueReceipt": true,
  "message": "string",
  "payment": {
    "cardBrand": "string",
    "cardCountry": "string",
    "cardExpiryMonth": 0,
    "cardExpiryYear": 0,
    "cardLast4Digits": "stri",
    "coverFee": true,
    "token": "string"
  },
  "teamId": 0,
  "pageType": "campaign",
  "template": {
    "key": "string",
    "value": {}
  },
  "type": "online"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Donation',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Donation', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Donation", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Donation`

*Creates a new donation*

> Body parameter

```json
{
  "amount": 0,
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "customer": {
    "anonymous": true,
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "businessName": "string",
    "email": "string",
    "firstName": "string",
    "fromCredential": true,
    "lastName": "string",
    "newsletter": true,
    "phoneNumber": "string"
  },
  "fundraiserId": 0,
  "issueReceipt": true,
  "message": "string",
  "payment": {
    "cardBrand": "string",
    "cardCountry": "string",
    "cardExpiryMonth": 0,
    "cardExpiryYear": 0,
    "cardLast4Digits": "stri",
    "coverFee": true,
    "token": "string"
  },
  "teamId": 0,
  "pageType": "campaign",
  "template": {
    "key": "string",
    "value": {}
  },
  "type": "online"
}
```

<h3 id="apiv2donationpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[DonationEditModel](#schemadonationeditmodel)|false|The donation model containing the details|

> Example responses

> 201 Response

```json
{
  "data": {
    "accountId": 0,
    "amount": 0,
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string",
      "template": {
        "key": "string",
        "value": {}
      }
    },
    "donatedAtLocal": "2018-08-20T06:00:18Z",
    "donatedAt": "2018-08-20T06:00:18Z",
    "donor": {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "anonymous": true,
      "businessName": "string",
      "donorId": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "newsletter": true,
      "phoneNumber": "string"
    },
    "financials": {
      "cardBrand": "string",
      "cardCountry": "string",
      "cardLast4Digits": "string",
      "currency": "string",
      "fee": 0,
      "feeCovered": true,
      "platform": "stripe",
      "refunded": true,
      "refundedAt": "2018-08-20T06:00:18Z",
      "refundedAtLocal": "2018-08-20T06:00:18Z",
      "subscription": true,
      "tax": 0,
      "totalFees": 0,
      "timezone": "string"
    },
    "fundraiserId": 0,
    "fundraiser": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAt": "2018-08-20T06:00:18Z",
    "message": "string",
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "pageType": "campaign",
    "receiptNumber": "string",
    "reply": {
      "displayFirstName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "repliedAtLocal": "2018-08-20T06:00:18Z",
      "repliedAt": "2018-08-20T06:00:18Z",
      "reply": "string"
    },
    "status": "collectedFromCustomer",
    "teamId": 0,
    "team": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "type": "online"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2DonationByIdReplyPost

<a id="opIdApiV2DonationByIdReplyPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Donation/{id}/reply \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Donation/{id}/reply HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/{id}/reply',
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
  "reply": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/{id}/reply',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Donation/{id}/reply',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Donation/{id}/reply', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/{id}/reply");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Donation/{id}/reply", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Donation/{id}/reply`

*Creates a new donation message reply*

> Body parameter

```json
{
  "reply": "string"
}
```

<h3 id="apiv2donationbyidreplypost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The donation id being replied to|
|body|body|[DonationMessageReplyEditModel](#schemadonationmessagereplyeditmodel)|false|The donation model containing the details|

> Example responses

> 201 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationbyidreplypost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationSearchPost

<a id="opIdApiV2DonationSearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Donation/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Donation/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Donation/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Donation/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Donation/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Donation/search`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2donationsearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[DonationSearchModel](#schemadonationsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "accountId": 0,
        "amount": 0,
        "campaignId": 0,
        "campaign": {
          "id": 0,
          "name": "string",
          "urlPath": "string",
          "url": "string",
          "template": {
            "key": "string",
            "value": {}
          }
        },
        "donatedAtLocal": "2018-08-20T06:00:18Z",
        "donatedAt": "2018-08-20T06:00:18Z",
        "donor": {
          "address": {
            "street": "string",
            "city": "string",
            "state": "string",
            "postcode": "string",
            "country": "string"
          },
          "anonymous": true,
          "businessName": "string",
          "donorId": 0,
          "email": "string",
          "firstName": "string",
          "lastName": "string",
          "newsletter": true,
          "phoneNumber": "string"
        },
        "financials": {
          "cardBrand": "string",
          "cardCountry": "string",
          "cardLast4Digits": "string",
          "currency": "string",
          "fee": 0,
          "feeCovered": true,
          "platform": "stripe",
          "refunded": true,
          "refundedAt": "2018-08-20T06:00:18Z",
          "refundedAtLocal": "2018-08-20T06:00:18Z",
          "subscription": true,
          "tax": 0,
          "totalFees": 0,
          "timezone": "string"
        },
        "fundraiserId": 0,
        "fundraiser": {
          "id": 0,
          "name": "string",
          "urlPath": "string",
          "url": "string"
        },
        "id": 0,
        "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
        "lastUpdatedAt": "2018-08-20T06:00:18Z",
        "message": "string",
        "organizationId": 0,
        "organization": {
          "id": 0,
          "name": "string",
          "urlPath": "string"
        },
        "pageType": "campaign",
        "receiptNumber": "string",
        "reply": {
          "displayFirstName": "string",
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "repliedAtLocal": "2018-08-20T06:00:18Z",
          "repliedAt": "2018-08-20T06:00:18Z",
          "reply": "string"
        },
        "status": "collectedFromCustomer",
        "teamId": 0,
        "team": {
          "id": 0,
          "name": "string",
          "urlPath": "string",
          "url": "string"
        },
        "template": {
          "key": "string",
          "value": {}
        },
        "timezone": "string",
        "type": "online"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationsearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_DonationElementModel_](#schemalistactionresult_donationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_DonationElementModel_](#schemalistactionresult_donationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationSearchPublicPost

<a id="opIdApiV2DonationSearchPublicPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Donation/search/public \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Donation/search/public HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/search/public',
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
  "primaryUrlPath": "string",
  "secondaryUrlPath": "string",
  "tertiaryUrlPath": "string",
  "page": 0
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/search/public',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Donation/search/public',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Donation/search/public', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/search/public");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Donation/search/public", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Donation/search/public`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "primaryUrlPath": "string",
  "secondaryUrlPath": "string",
  "tertiaryUrlPath": "string",
  "page": 0
}
```

<h3 id="apiv2donationsearchpublicpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[DonationPublicSearchModel](#schemadonationpublicsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "amount": 0,
        "anonymous": true,
        "donatedAtLocal": "2018-08-20T06:00:18Z",
        "donatedAt": "2018-08-20T06:00:18Z",
        "donorDisplayName": "string",
        "id": 0,
        "message": "string",
        "pageType": "campaign",
        "reply": {
          "displayFirstName": "string",
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "repliedAtLocal": "2018-08-20T06:00:18Z",
          "repliedAt": "2018-08-20T06:00:18Z",
          "reply": "string"
        },
        "type": "online"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationsearchpublicpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_DonationPublicResultModel_](#schemalistactionresult_donationpublicresultmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_DonationPublicResultModel_](#schemalistactionresult_donationpublicresultmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2DonationExportPost

<a id="opIdApiV2DonationExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Donation/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Donation/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Donation/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Donation/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Donation/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Donation/export`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2donationexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[DonationSearchModel](#schemadonationsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationMetadataGet

<a id="opIdApiV2DonationMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Donation/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Donation/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Donation/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Donation/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Donation/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Donation/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationmetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationAggregateGet

<a id="opIdApiV2DonationAggregateGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Donation/aggregate \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Donation/aggregate HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/aggregate',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/aggregate',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Donation/aggregate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Donation/aggregate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/aggregate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Donation/aggregate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Donation/aggregate`

*Perform an aggregate function on a field based on a filter/custom-text criteria*

<h3 id="apiv2donationaggregateget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|fieldName|query|string|false|none|
|fieldAggregate|query|string|false|none|
|filters|query|array[any]|false|none|
|text|query|string|false|none|
|orderBy.key|query|string|false|none|
|orderBy.direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|pageSize|query|integer(int32)|false|none|
|resultType|query|string|false|none|
|includeDataTemplate|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|fieldAggregate|sum|
|fieldAggregate|average|
|fieldAggregate|min|
|fieldAggregate|max|
|fieldAggregate|count|
|orderBy.direction|asc|
|orderBy.direction|desc|
|resultType|lookup|
|resultType|basic|
|resultType|full|

> Example responses

> 200 Response

```json
{
  "data": 0,
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationaggregateget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationByIdRefundPost

<a id="opIdApiV2DonationByIdRefundPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Donation/{id}/refund \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Donation/{id}/refund HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/{id}/refund',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/{id}/refund',
{
  method: 'POST',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Donation/{id}/refund',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Donation/{id}/refund', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/{id}/refund");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Donation/{id}/refund", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Donation/{id}/refund`

*Perform a refund on an online donation*

<h3 id="apiv2donationbyidrefundpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|id of the donation being refunded|

> Example responses

> 200 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationbyidrefundpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationByIdReceiptPost

<a id="opIdApiV2DonationByIdReceiptPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Donation/{id}/receipt \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Donation/{id}/receipt HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Donation/{id}/receipt',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Donation/{id}/receipt',
{
  method: 'POST',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Donation/{id}/receipt',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Donation/{id}/receipt', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Donation/{id}/receipt");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Donation/{id}/receipt", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Donation/{id}/receipt`

*Perform a refund on an online donation*

<h3 id="apiv2donationbyidreceiptpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|id of the donation being refunded|

> Example responses

> 200 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationbyidreceiptpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-DonationFee">DonationFee</h1>

## ApiV2DonationFeeByIdGet

<a id="opIdApiV2DonationFeeByIdGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/DonationFee/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/DonationFee/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/DonationFee/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/DonationFee/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/DonationFee/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/DonationFee/{id}`

*Gets a donation fee object by id*

<h3 id="apiv2donationfeebyidget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Donation id|

> Example responses

> 200 Response

```json
{
  "data": {
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string"
    },
    "eventId": 0,
    "event": {
      "id": 0,
      "name": "string"
    },
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string"
    },
    "fee": 0,
    "feeType": "flatPercentage"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationfeebyidget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_DonationFeeElementModel_](#schemascalaractionresult_donationfeeelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_DonationFeeElementModel_](#schemascalaractionresult_donationfeeelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationFeeByIdPut

<a id="opIdApiV2DonationFeeByIdPut"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT //api.dev.grassrootz.com//api/v2/DonationFee/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PUT //api.dev.grassrootz.com//api/v2/DonationFee/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "organizationId": 0,
  "campaignId": 0,
  "eventId": 0,
  "fee": 0
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
{
  method: 'PUT',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.put '//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.put('//api.dev.grassrootz.com//api/v2/DonationFee/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/DonationFee/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "//api.dev.grassrootz.com//api/v2/DonationFee/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v2/DonationFee/{id}`

*Updates a donation fee object by id*

> Body parameter

```json
{
  "organizationId": 0,
  "campaignId": 0,
  "eventId": 0,
  "fee": 0
}
```

<h3 id="apiv2donationfeebyidput-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the donation fee object being modified|
|body|body|[DonationFeeEditModel](#schemadonationfeeeditmodel)|false|The donation fee model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string"
    },
    "eventId": 0,
    "event": {
      "id": 0,
      "name": "string"
    },
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string"
    },
    "fee": 0,
    "feeType": "flatPercentage"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationfeebyidput-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_DonationFeeElementModel_](#schemascalaractionresult_donationfeeelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_DonationFeeElementModel_](#schemascalaractionresult_donationfeeelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationFeeByIdDelete

<a id="opIdApiV2DonationFeeByIdDelete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE //api.dev.grassrootz.com//api/v2/DonationFee/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
DELETE //api.dev.grassrootz.com//api/v2/DonationFee/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
{
  method: 'DELETE',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.delete '//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.delete('//api.dev.grassrootz.com//api/v2/DonationFee/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/DonationFee/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "//api.dev.grassrootz.com//api/v2/DonationFee/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/DonationFee/{id}`

*Patches (partial update) a donation fee object by id*

<h3 id="apiv2donationfeebyiddelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the donation fee object being modified|

> Example responses

> 200 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationfeebyiddelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationFeeByIdPatch

<a id="opIdApiV2DonationFeeByIdPatch"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH //api.dev.grassrootz.com//api/v2/DonationFee/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PATCH //api.dev.grassrootz.com//api/v2/DonationFee/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
  method: 'patch',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
{
  method: 'PATCH',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.patch '//api.dev.grassrootz.com//api/v2/DonationFee/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.patch('//api.dev.grassrootz.com//api/v2/DonationFee/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/DonationFee/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "//api.dev.grassrootz.com//api/v2/DonationFee/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v2/DonationFee/{id}`

*Patches (partial update) a donation fee object by id*

> Body parameter

```json
[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]
```

<h3 id="apiv2donationfeebyidpatch-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the donation fee object being modified|
|body|body|array[object]|false|The donation fee model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "accountId": 0,
    "amount": 0,
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string",
      "template": {
        "key": "string",
        "value": {}
      }
    },
    "donatedAtLocal": "2018-08-20T06:00:18Z",
    "donatedAt": "2018-08-20T06:00:18Z",
    "donor": {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "anonymous": true,
      "businessName": "string",
      "donorId": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "newsletter": true,
      "phoneNumber": "string"
    },
    "financials": {
      "cardBrand": "string",
      "cardCountry": "string",
      "cardLast4Digits": "string",
      "currency": "string",
      "fee": 0,
      "feeCovered": true,
      "platform": "stripe",
      "refunded": true,
      "refundedAt": "2018-08-20T06:00:18Z",
      "refundedAtLocal": "2018-08-20T06:00:18Z",
      "subscription": true,
      "tax": 0,
      "totalFees": 0,
      "timezone": "string"
    },
    "fundraiserId": 0,
    "fundraiser": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAt": "2018-08-20T06:00:18Z",
    "message": "string",
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "pageType": "campaign",
    "receiptNumber": "string",
    "reply": {
      "displayFirstName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "repliedAtLocal": "2018-08-20T06:00:18Z",
      "repliedAt": "2018-08-20T06:00:18Z",
      "reply": "string"
    },
    "status": "collectedFromCustomer",
    "teamId": 0,
    "team": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "type": "online"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationfeebyidpatch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationFeePost

<a id="opIdApiV2DonationFeePost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/DonationFee \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/DonationFee HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/DonationFee',
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
  "organizationId": 0,
  "campaignId": 0,
  "eventId": 0,
  "fee": 0
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/DonationFee',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/DonationFee',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/DonationFee', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/DonationFee");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/DonationFee", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/DonationFee`

*Creates a new donation fee*

> Body parameter

```json
{
  "organizationId": 0,
  "campaignId": 0,
  "eventId": 0,
  "fee": 0
}
```

<h3 id="apiv2donationfeepost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[DonationFeeEditModel](#schemadonationfeeeditmodel)|false|The donation fee model containing the details|

> Example responses

> 201 Response

```json
{
  "data": {
    "accountId": 0,
    "amount": 0,
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string",
      "template": {
        "key": "string",
        "value": {}
      }
    },
    "donatedAtLocal": "2018-08-20T06:00:18Z",
    "donatedAt": "2018-08-20T06:00:18Z",
    "donor": {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "anonymous": true,
      "businessName": "string",
      "donorId": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "newsletter": true,
      "phoneNumber": "string"
    },
    "financials": {
      "cardBrand": "string",
      "cardCountry": "string",
      "cardLast4Digits": "string",
      "currency": "string",
      "fee": 0,
      "feeCovered": true,
      "platform": "stripe",
      "refunded": true,
      "refundedAt": "2018-08-20T06:00:18Z",
      "refundedAtLocal": "2018-08-20T06:00:18Z",
      "subscription": true,
      "tax": 0,
      "totalFees": 0,
      "timezone": "string"
    },
    "fundraiserId": 0,
    "fundraiser": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAt": "2018-08-20T06:00:18Z",
    "message": "string",
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "pageType": "campaign",
    "receiptNumber": "string",
    "reply": {
      "displayFirstName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "repliedAtLocal": "2018-08-20T06:00:18Z",
      "repliedAt": "2018-08-20T06:00:18Z",
      "reply": "string"
    },
    "status": "collectedFromCustomer",
    "teamId": 0,
    "team": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "type": "online"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationfeepost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_DonationElementModel_](#schemascalaractionresult_donationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationFeeSearchPost

<a id="opIdApiV2DonationFeeSearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/DonationFee/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/DonationFee/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/DonationFee/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/DonationFee/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/DonationFee/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/DonationFee/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/DonationFee/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/DonationFee/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/DonationFee/search`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2donationfeesearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[DonationFeeSearchModel](#schemadonationfeesearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "organizationId": 0,
        "organization": {
          "id": 0,
          "name": "string"
        },
        "eventId": 0,
        "event": {
          "id": 0,
          "name": "string"
        },
        "campaignId": 0,
        "campaign": {
          "id": 0,
          "name": "string"
        },
        "fee": 0,
        "feeType": "flatPercentage"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationfeesearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_DonationFeeElementModel_](#schemalistactionresult_donationfeeelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_DonationFeeElementModel_](#schemalistactionresult_donationfeeelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationFeeExportGet

<a id="opIdApiV2DonationFeeExportGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/DonationFee/export \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/DonationFee/export HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/DonationFee/export',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/DonationFee/export',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/DonationFee/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/DonationFee/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/DonationFee/export");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/DonationFee/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/DonationFee/export`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

<h3 id="apiv2donationfeeexportget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|filters|query|array[any]|false|none|
|text|query|string|false|none|
|orderBy.key|query|string|false|none|
|orderBy.direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|pageSize|query|integer(int32)|false|none|
|resultType|query|string|false|none|
|includeDataTemplate|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|orderBy.direction|asc|
|orderBy.direction|desc|
|resultType|lookup|
|resultType|basic|
|resultType|full|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationfeeexportget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationFeeExportPost

<a id="opIdApiV2DonationFeeExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/DonationFee/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/DonationFee/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/DonationFee/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/DonationFee/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/DonationFee/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/DonationFee/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/DonationFee/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/DonationFee/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/DonationFee/export`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2donationfeeexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[DonationFeeSearchModel](#schemadonationfeesearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationfeeexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2DonationFeeMetadataGet

<a id="opIdApiV2DonationFeeMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/DonationFee/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/DonationFee/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/DonationFee/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/DonationFee/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/DonationFee/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/DonationFee/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/DonationFee/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/DonationFee/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/DonationFee/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2donationfeemetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-Event">Event</h1>

## ApiV2PageEventByIdGet

<a id="opIdApiV2PageEventByIdGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Event/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Event/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Event/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Event/{id}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Event/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Event/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Event/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Event/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Event/{id}`

*Gets a event object by id*

<h3 id="apiv2pageeventbyidget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Event id|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 0,
    "organizationId": 0,
    "organizationFee": 0,
    "name": "string",
    "createdAt": "2018-08-20T06:00:18Z",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "urlPath": "string",
    "status": "live",
    "targetAmount": 0,
    "averageDonationAmount": 0,
    "raisedAmount": 0,
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "organizations": [
      {
        "id": 0,
        "name": "string",
        "priority": "Tertiary"
      }
    ],
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "fields": {
      "Registration": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ],
      "Donation": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ],
      "Ticket": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ]
    },
    "template": {
      "key": "string",
      "value": {}
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageeventbyidget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_EventElementModel_](#schemascalaractionresult_eventelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_EventElementModel_](#schemascalaractionresult_eventelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageEventByIdPut

<a id="opIdApiV2PageEventByIdPut"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT //api.dev.grassrootz.com//api/v2/page/Event/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PUT //api.dev.grassrootz.com//api/v2/page/Event/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Event/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "organizationId": 0,
  "organizationFee": 0,
  "name": "string",
  "mainImagePath": "string",
  "urlPath": "string",
  "status": "live",
  "targetAmount": 0,
  "fields": {
    "Registration": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Donation": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Ticket": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ]
  },
  "organizations": [
    {
      "id": 0,
      "priority": "Tertiary"
    }
  ],
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "external": {
    "system": "active",
    "registrationUrl": "string",
    "id": "string"
  },
  "template": {
    "key": "string",
    "value": {}
  }
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Event/{id}',
{
  method: 'PUT',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.put '//api.dev.grassrootz.com//api/v2/page/Event/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.put('//api.dev.grassrootz.com//api/v2/page/Event/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Event/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "//api.dev.grassrootz.com//api/v2/page/Event/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v2/page/Event/{id}`

*Updates a event object by id*

> Body parameter

```json
{
  "organizationId": 0,
  "organizationFee": 0,
  "name": "string",
  "mainImagePath": "string",
  "urlPath": "string",
  "status": "live",
  "targetAmount": 0,
  "fields": {
    "Registration": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Donation": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Ticket": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ]
  },
  "organizations": [
    {
      "id": 0,
      "priority": "Tertiary"
    }
  ],
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "external": {
    "system": "active",
    "registrationUrl": "string",
    "id": "string"
  },
  "template": {
    "key": "string",
    "value": {}
  }
}
```

<h3 id="apiv2pageeventbyidput-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the event object being modified|
|body|body|[EventEditModel](#schemaeventeditmodel)|false|The event model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 0,
    "organizationId": 0,
    "organizationFee": 0,
    "name": "string",
    "createdAt": "2018-08-20T06:00:18Z",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "urlPath": "string",
    "status": "live",
    "targetAmount": 0,
    "averageDonationAmount": 0,
    "raisedAmount": 0,
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "organizations": [
      {
        "id": 0,
        "name": "string",
        "priority": "Tertiary"
      }
    ],
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "fields": {
      "Registration": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ],
      "Donation": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ],
      "Ticket": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ]
    },
    "template": {
      "key": "string",
      "value": {}
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageeventbyidput-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_EventElementModel_](#schemascalaractionresult_eventelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_EventElementModel_](#schemascalaractionresult_eventelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageEventByIdDelete

<a id="opIdApiV2PageEventByIdDelete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE //api.dev.grassrootz.com//api/v2/page/Event/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
DELETE //api.dev.grassrootz.com//api/v2/page/Event/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Event/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Event/{id}',
{
  method: 'DELETE',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.delete '//api.dev.grassrootz.com//api/v2/page/Event/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.delete('//api.dev.grassrootz.com//api/v2/page/Event/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Event/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "//api.dev.grassrootz.com//api/v2/page/Event/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/page/Event/{id}`

*Patches (partial update) a event object by id*

<h3 id="apiv2pageeventbyiddelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the event object being modified|

> Example responses

> 200 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageeventbyiddelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageEventByIdPatch

<a id="opIdApiV2PageEventByIdPatch"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH //api.dev.grassrootz.com//api/v2/page/Event/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PATCH //api.dev.grassrootz.com//api/v2/page/Event/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Event/{id}',
  method: 'patch',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Event/{id}',
{
  method: 'PATCH',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.patch '//api.dev.grassrootz.com//api/v2/page/Event/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.patch('//api.dev.grassrootz.com//api/v2/page/Event/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Event/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "//api.dev.grassrootz.com//api/v2/page/Event/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v2/page/Event/{id}`

*Patches (partial update) a event object by id*

> Body parameter

```json
[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]
```

<h3 id="apiv2pageeventbyidpatch-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the event object being modified|
|body|body|array[object]|false|The event model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "id": 0,
    "organizationId": 0,
    "organizationFee": 0,
    "name": "string",
    "createdAt": "2018-08-20T06:00:18Z",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "urlPath": "string",
    "status": "live",
    "targetAmount": 0,
    "averageDonationAmount": 0,
    "raisedAmount": 0,
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "organizations": [
      {
        "id": 0,
        "name": "string",
        "priority": "Tertiary"
      }
    ],
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "fields": {
      "Registration": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ],
      "Donation": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ],
      "Ticket": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ]
    },
    "template": {
      "key": "string",
      "value": {}
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageeventbyidpatch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_EventElementModel_](#schemascalaractionresult_eventelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_EventElementModel_](#schemascalaractionresult_eventelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageEventPost

<a id="opIdApiV2PageEventPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Event \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Event HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Event',
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
  "organizationId": 0,
  "organizationFee": 0,
  "name": "string",
  "mainImagePath": "string",
  "urlPath": "string",
  "status": "live",
  "targetAmount": 0,
  "fields": {
    "Registration": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Donation": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Ticket": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ]
  },
  "organizations": [
    {
      "id": 0,
      "priority": "Tertiary"
    }
  ],
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "external": {
    "system": "active",
    "registrationUrl": "string",
    "id": "string"
  },
  "template": {
    "key": "string",
    "value": {}
  }
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Event',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Event',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Event', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Event");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Event", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Event`

*Creates a new event*

> Body parameter

```json
{
  "organizationId": 0,
  "organizationFee": 0,
  "name": "string",
  "mainImagePath": "string",
  "urlPath": "string",
  "status": "live",
  "targetAmount": 0,
  "fields": {
    "Registration": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Donation": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Ticket": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ]
  },
  "organizations": [
    {
      "id": 0,
      "priority": "Tertiary"
    }
  ],
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "external": {
    "system": "active",
    "registrationUrl": "string",
    "id": "string"
  },
  "template": {
    "key": "string",
    "value": {}
  }
}
```

<h3 id="apiv2pageeventpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[EventEditModel](#schemaeventeditmodel)|false|The event model containing the details|

> Example responses

> 201 Response

```json
{
  "data": {
    "id": 0,
    "organizationId": 0,
    "organizationFee": 0,
    "name": "string",
    "createdAt": "2018-08-20T06:00:18Z",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "urlPath": "string",
    "status": "live",
    "targetAmount": 0,
    "averageDonationAmount": 0,
    "raisedAmount": 0,
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "organizations": [
      {
        "id": 0,
        "name": "string",
        "priority": "Tertiary"
      }
    ],
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "fields": {
      "Registration": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ],
      "Donation": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ],
      "Ticket": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ]
    },
    "template": {
      "key": "string",
      "value": {}
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageeventpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_EventElementModel_](#schemascalaractionresult_eventelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_EventElementModel_](#schemascalaractionresult_eventelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageEventSearchPost

<a id="opIdApiV2PageEventSearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Event/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Event/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Event/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Event/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Event/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Event/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Event/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Event/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Event/search`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2pageeventsearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[EventSearchModel](#schemaeventsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "id": 0,
        "organizationId": 0,
        "organizationFee": 0,
        "name": "string",
        "createdAt": "2018-08-20T06:00:18Z",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "urlPath": "string",
        "status": "live",
        "targetAmount": 0,
        "averageDonationAmount": 0,
        "raisedAmount": 0,
        "donationCount": 0,
        "donationSetup": {
          "allowRecurringGiving": true
        },
        "organizations": [
          {
            "id": 0,
            "name": "string",
            "priority": "Tertiary"
          }
        ],
        "fundraisers": {
          "enabled": true,
          "defaultTargetAmount": 0,
          "allowSelfSignUp": true
        },
        "teams": {
          "enabled": true,
          "defaultTargetAmount": 0,
          "allowSelfSignUp": true
        },
        "fields": {
          "Registration": [
            {
              "identifier": "string",
              "type": "text",
              "label": "string",
              "mandatory": true
            }
          ],
          "Donation": [
            {
              "identifier": "string",
              "type": "text",
              "label": "string",
              "mandatory": true
            }
          ],
          "Ticket": [
            {
              "identifier": "string",
              "type": "text",
              "label": "string",
              "mandatory": true
            }
          ]
        },
        "template": {
          "key": "string",
          "value": {}
        }
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageeventsearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_EventElementModel_](#schemalistactionresult_eventelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_EventElementModel_](#schemalistactionresult_eventelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageEventExportPost

<a id="opIdApiV2PageEventExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Event/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Event/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Event/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Event/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Event/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Event/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Event/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Event/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Event/export`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2pageeventexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[EventSearchModel](#schemaeventsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageeventexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageEventMetadataGet

<a id="opIdApiV2PageEventMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Event/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Event/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Event/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Event/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Event/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Event/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Event/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Event/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Event/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageeventmetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageEventAggregateGet

<a id="opIdApiV2PageEventAggregateGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Event/aggregate \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Event/aggregate HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Event/aggregate',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Event/aggregate',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Event/aggregate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Event/aggregate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Event/aggregate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Event/aggregate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Event/aggregate`

*Perform an aggregate function on a field based on a filter/custom-text criteria*

<h3 id="apiv2pageeventaggregateget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|fieldName|query|string|false|none|
|fieldAggregate|query|string|false|none|
|filters|query|array[any]|false|none|
|text|query|string|false|none|
|orderBy.key|query|string|false|none|
|orderBy.direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|pageSize|query|integer(int32)|false|none|
|resultType|query|string|false|none|
|includeDataTemplate|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|fieldAggregate|sum|
|fieldAggregate|average|
|fieldAggregate|min|
|fieldAggregate|max|
|fieldAggregate|count|
|orderBy.direction|asc|
|orderBy.direction|desc|
|resultType|lookup|
|resultType|basic|
|resultType|full|

> Example responses

> 200 Response

```json
{
  "data": 0,
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageeventaggregateget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-Fundraiser">Fundraiser</h1>

## ApiV2PageFundraiserByIdGet

<a id="opIdApiV2PageFundraiserByIdGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Fundraiser/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Fundraiser/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Fundraiser/{id}`

*Gets a fundraiser object by id*

<h3 id="apiv2pagefundraiserbyidget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Fundraiser id|

> Example responses

> 200 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "averageDonationAmount": 0,
    "campaignId": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "manager": {
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "id": 0
    },
    "name": "string",
    "newsletter": true,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "phoneNumber": "string",
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "teamId": 0,
    "team": {
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "urlPath": "string",
    "url": "string",
    "urlFull": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagefundraiserbyidget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_FundraiserElementModel_](#schemascalaractionresult_fundraiserelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_FundraiserElementModel_](#schemascalaractionresult_fundraiserelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageFundraiserByIdPut

<a id="opIdApiV2PageFundraiserByIdPut"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT //api.dev.grassrootz.com//api/v2/page/Fundraiser/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PUT //api.dev.grassrootz.com//api/v2/page/Fundraiser/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "isPublic": true,
  "mainImagePath": "string",
  "manager": {
    "operation": "unchanged",
    "email": "string",
    "customInviteUrl": "string"
  },
  "name": "string",
  "newsletter": true,
  "phoneNumber": "string",
  "status": "live",
  "targetAmount": 0,
  "teamId": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "urlPath": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
{
  method: 'PUT',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.put '//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.put('//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v2/page/Fundraiser/{id}`

*Updates a fundraiser object by id*

> Body parameter

```json
{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "isPublic": true,
  "mainImagePath": "string",
  "manager": {
    "operation": "unchanged",
    "email": "string",
    "customInviteUrl": "string"
  },
  "name": "string",
  "newsletter": true,
  "phoneNumber": "string",
  "status": "live",
  "targetAmount": 0,
  "teamId": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "urlPath": "string"
}
```

<h3 id="apiv2pagefundraiserbyidput-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the fundraiser object being modified|
|body|body|[FundraiserEditModel](#schemafundraisereditmodel)|false|The fundraiser model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "averageDonationAmount": 0,
    "campaignId": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "manager": {
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "id": 0
    },
    "name": "string",
    "newsletter": true,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "phoneNumber": "string",
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "teamId": 0,
    "team": {
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "urlPath": "string",
    "url": "string",
    "urlFull": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagefundraiserbyidput-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_FundraiserElementModel_](#schemascalaractionresult_fundraiserelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_FundraiserElementModel_](#schemascalaractionresult_fundraiserelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageFundraiserByIdDelete

<a id="opIdApiV2PageFundraiserByIdDelete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE //api.dev.grassrootz.com//api/v2/page/Fundraiser/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
DELETE //api.dev.grassrootz.com//api/v2/page/Fundraiser/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
{
  method: 'DELETE',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.delete '//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.delete('//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/page/Fundraiser/{id}`

*Patches (partial update) a fundraiser object by id*

<h3 id="apiv2pagefundraiserbyiddelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the fundraiser object being deleted|

> Example responses

> 200 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagefundraiserbyiddelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageFundraiserByIdPatch

<a id="opIdApiV2PageFundraiserByIdPatch"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH //api.dev.grassrootz.com//api/v2/page/Fundraiser/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PATCH //api.dev.grassrootz.com//api/v2/page/Fundraiser/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
  method: 'patch',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
{
  method: 'PATCH',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.patch '//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.patch('//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "//api.dev.grassrootz.com//api/v2/page/Fundraiser/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v2/page/Fundraiser/{id}`

*Patches (partial update) a fundraiser object by id*

> Body parameter

```json
[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]
```

<h3 id="apiv2pagefundraiserbyidpatch-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the fundraiser object being modified|
|body|body|array[object]|false|The fundraiser model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "averageDonationAmount": 0,
    "campaignId": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "manager": {
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "id": 0
    },
    "name": "string",
    "newsletter": true,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "phoneNumber": "string",
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "teamId": 0,
    "team": {
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "urlPath": "string",
    "url": "string",
    "urlFull": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagefundraiserbyidpatch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_FundraiserElementModel_](#schemascalaractionresult_fundraiserelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_FundraiserElementModel_](#schemascalaractionresult_fundraiserelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageFundraiserOwnerByIdHead

<a id="opIdApiV2PageFundraiserOwnerByIdHead"></a>

> Code samples

```shell
# You can also use wget
curl -X HEAD //api.dev.grassrootz.com//api/v2/page/Fundraiser/owner/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
HEAD //api.dev.grassrootz.com//api/v2/page/Fundraiser/owner/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Fundraiser/owner/{id}',
  method: 'head',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Fundraiser/owner/{id}',
{
  method: 'HEAD',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.head '//api.dev.grassrootz.com//api/v2/page/Fundraiser/owner/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.head('//api.dev.grassrootz.com//api/v2/page/Fundraiser/owner/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Fundraiser/owner/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("HEAD");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("HEAD", "//api.dev.grassrootz.com//api/v2/page/Fundraiser/owner/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`HEAD /api/v2/page/Fundraiser/owner/{id}`

*Checks a fundraiser owner via id*

<h3 id="apiv2pagefundraiserownerbyidhead-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Fundraiser id|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="apiv2pagefundraiserownerbyidhead-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageFundraiserPublicByPrimaryPathBySecondaryPathByUrlPathGet

<a id="opIdApiV2PageFundraiserPublicByPrimaryPathBySecondaryPathByUrlPathGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Fundraiser/public/{primaryPath}/{secondaryPath}/{urlPath} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Fundraiser/public/{primaryPath}/{secondaryPath}/{urlPath} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Fundraiser/public/{primaryPath}/{secondaryPath}/{urlPath}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Fundraiser/public/{primaryPath}/{secondaryPath}/{urlPath}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Fundraiser/public/{primaryPath}/{secondaryPath}/{urlPath}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Fundraiser/public/{primaryPath}/{secondaryPath}/{urlPath}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Fundraiser/public/{primaryPath}/{secondaryPath}/{urlPath}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Fundraiser/public/{primaryPath}/{secondaryPath}/{urlPath}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Fundraiser/public/{primaryPath}/{secondaryPath}/{urlPath}`

*Gets a fundraiser object by paths*

<h3 id="apiv2pagefundraiserpublicbyprimarypathbysecondarypathbyurlpathget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|primaryPath|path|string|true|Primary (Event or Organization) Url Path|
|secondaryPath|path|string|true|Secondary (Campaign or Organization) Url Path|
|urlPath|path|string|true|Fundraiser Url Path|

> Example responses

> 200 Response

```json
{
  "data": {
    "averageDonationAmount": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "team": {
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "targetAmount": 0,
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "template": {
      "value": {
        "property1": {},
        "property2": {}
      }
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagefundraiserpublicbyprimarypathbysecondarypathbyurlpathget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_FundraiserPublicModel_](#schemascalaractionresult_fundraiserpublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_FundraiserPublicModel_](#schemascalaractionresult_fundraiserpublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2PageFundraiserPost

<a id="opIdApiV2PageFundraiserPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Fundraiser \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Fundraiser HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Fundraiser',
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
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "isPublic": true,
  "mainImagePath": "string",
  "manager": {
    "operation": "unchanged",
    "email": "string",
    "customInviteUrl": "string"
  },
  "name": "string",
  "newsletter": true,
  "phoneNumber": "string",
  "status": "live",
  "targetAmount": 0,
  "teamId": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "urlPath": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Fundraiser',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Fundraiser',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Fundraiser', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Fundraiser");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Fundraiser", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Fundraiser`

*Creates a new fundraiser*

> Body parameter

```json
{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "isPublic": true,
  "mainImagePath": "string",
  "manager": {
    "operation": "unchanged",
    "email": "string",
    "customInviteUrl": "string"
  },
  "name": "string",
  "newsletter": true,
  "phoneNumber": "string",
  "status": "live",
  "targetAmount": 0,
  "teamId": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "urlPath": "string"
}
```

<h3 id="apiv2pagefundraiserpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[FundraiserEditModel](#schemafundraisereditmodel)|false|The fundraiser model containing the details|

> Example responses

> 201 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "averageDonationAmount": 0,
    "campaignId": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "manager": {
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "id": 0
    },
    "name": "string",
    "newsletter": true,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "phoneNumber": "string",
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "teamId": 0,
    "team": {
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "urlPath": "string",
    "url": "string",
    "urlFull": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagefundraiserpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_FundraiserElementModel_](#schemascalaractionresult_fundraiserelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_FundraiserElementModel_](#schemascalaractionresult_fundraiserelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageFundraiserSearchPost

<a id="opIdApiV2PageFundraiserSearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Fundraiser/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Fundraiser/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Fundraiser/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Fundraiser/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Fundraiser/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Fundraiser/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Fundraiser/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Fundraiser/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Fundraiser/search`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2pagefundraisersearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[FundraiserSearchModel](#schemafundraisersearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "address": {
          "street": "string",
          "city": "string",
          "state": "string",
          "postcode": "string",
          "country": "string"
        },
        "averageDonationAmount": 0,
        "campaignId": 0,
        "campaign": {
          "allowsFundraisers": true,
          "allowsFundraiserSelfSignUp": true,
          "allowsTeams": true,
          "allowsTeamSelfSignUp": true,
          "donationCount": 0,
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "raisedAmount": 0,
          "status": "live",
          "targetAmount": 0,
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "donationCount": 0,
        "id": 0,
        "isPublic": true,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "manager": {
          "email": "string",
          "firstName": "string",
          "lastName": "string",
          "id": 0
        },
        "name": "string",
        "newsletter": true,
        "organization": {
          "country": "string",
          "currency": "string",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "phoneNumber": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "teamId": 0,
        "team": {
          "donationCount": 0,
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "raisedAmount": 0,
          "targetAmount": 0,
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "template": {
          "key": "string",
          "value": {}
        },
        "urlPath": "string",
        "url": "string",
        "urlFull": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagefundraisersearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_FundraiserElementModel_](#schemalistactionresult_fundraiserelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_FundraiserElementModel_](#schemalistactionresult_fundraiserelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageFundraiserExportPost

<a id="opIdApiV2PageFundraiserExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Fundraiser/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Fundraiser/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Fundraiser/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Fundraiser/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Fundraiser/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Fundraiser/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Fundraiser/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Fundraiser/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Fundraiser/export`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2pagefundraiserexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[FundraiserSearchModel](#schemafundraisersearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagefundraiserexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageFundraiserMetadataGet

<a id="opIdApiV2PageFundraiserMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Fundraiser/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Fundraiser/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Fundraiser/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Fundraiser/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Fundraiser/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Fundraiser/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Fundraiser/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Fundraiser/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Fundraiser/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagefundraisermetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageFundraiserAggregateGet

<a id="opIdApiV2PageFundraiserAggregateGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Fundraiser/aggregate \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Fundraiser/aggregate HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Fundraiser/aggregate',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Fundraiser/aggregate',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Fundraiser/aggregate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Fundraiser/aggregate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Fundraiser/aggregate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Fundraiser/aggregate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Fundraiser/aggregate`

*Perform an aggregate function on a field based on a filter/custom-text criteria*

<h3 id="apiv2pagefundraiseraggregateget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|fieldName|query|string|false|none|
|fieldAggregate|query|string|false|none|
|filters|query|array[any]|false|none|
|text|query|string|false|none|
|orderBy.key|query|string|false|none|
|orderBy.direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|pageSize|query|integer(int32)|false|none|
|resultType|query|string|false|none|
|includeDataTemplate|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|fieldAggregate|sum|
|fieldAggregate|average|
|fieldAggregate|min|
|fieldAggregate|max|
|fieldAggregate|count|
|orderBy.direction|asc|
|orderBy.direction|desc|
|resultType|lookup|
|resultType|basic|
|resultType|full|

> Example responses

> 200 Response

```json
{
  "data": 0,
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagefundraiseraggregateget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-Organization">Organization</h1>

## ApiV2OrganizationByIdGet

<a id="opIdApiV2OrganizationByIdGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Organization/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Organization/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/{id}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Organization/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Organization/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Organization/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Organization/{id}`

*Gets an organization object by id*

<h3 id="apiv2organizationbyidget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Organization id|

> Example responses

> 200 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "currency": "string",
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "fundraisingPageCreatedEmail": "string",
    "id": 0,
    "legalName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "newDonationEmail": "string",
    "newInvoiceEmail": "string",
    "paymentPlatforms": [
      {
        "id": 0,
        "type": "creditCardForm",
        "platform": "stripe"
      }
    ],
    "taxId": "string",
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2organizationbyidget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_OrganizationElementModel_](#schemascalaractionresult_organizationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_OrganizationElementModel_](#schemascalaractionresult_organizationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationByIdPut

<a id="opIdApiV2OrganizationByIdPut"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT //api.dev.grassrootz.com//api/v2/Organization/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PUT //api.dev.grassrootz.com//api/v2/Organization/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "name": "string",
  "mainImagePath": "string",
  "legalName": "string",
  "taxId": "string",
  "urlPath": "string",
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "timezone": "string",
  "adminEmail": "string",
  "fundraisingPageCreatedEmail": "string",
  "newDonationEmail": "string",
  "newInvoiceEmail": "string",
  "template": {
    "key": "string",
    "value": {}
  }
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/{id}',
{
  method: 'PUT',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.put '//api.dev.grassrootz.com//api/v2/Organization/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.put('//api.dev.grassrootz.com//api/v2/Organization/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "//api.dev.grassrootz.com//api/v2/Organization/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v2/Organization/{id}`

*Updates an organization object by id*

> Body parameter

```json
{
  "name": "string",
  "mainImagePath": "string",
  "legalName": "string",
  "taxId": "string",
  "urlPath": "string",
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "timezone": "string",
  "adminEmail": "string",
  "fundraisingPageCreatedEmail": "string",
  "newDonationEmail": "string",
  "newInvoiceEmail": "string",
  "template": {
    "key": "string",
    "value": {}
  }
}
```

<h3 id="apiv2organizationbyidput-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the organization object being modified|
|body|body|[OrganizationEditModel](#schemaorganizationeditmodel)|false|The organization model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "currency": "string",
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "fundraisingPageCreatedEmail": "string",
    "id": 0,
    "legalName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "newDonationEmail": "string",
    "newInvoiceEmail": "string",
    "paymentPlatforms": [
      {
        "id": 0,
        "type": "creditCardForm",
        "platform": "stripe"
      }
    ],
    "taxId": "string",
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2organizationbyidput-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_OrganizationElementModel_](#schemascalaractionresult_organizationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_OrganizationElementModel_](#schemascalaractionresult_organizationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationByIdDelete

<a id="opIdApiV2OrganizationByIdDelete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE //api.dev.grassrootz.com//api/v2/Organization/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
DELETE //api.dev.grassrootz.com//api/v2/Organization/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/{id}',
{
  method: 'DELETE',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.delete '//api.dev.grassrootz.com//api/v2/Organization/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.delete('//api.dev.grassrootz.com//api/v2/Organization/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "//api.dev.grassrootz.com//api/v2/Organization/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/Organization/{id}`

*Patches (partial update) an organization object by id*

<h3 id="apiv2organizationbyiddelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the organization object being modified|

> Example responses

> 200 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2organizationbyiddelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationByIdPatch

<a id="opIdApiV2OrganizationByIdPatch"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH //api.dev.grassrootz.com//api/v2/Organization/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PATCH //api.dev.grassrootz.com//api/v2/Organization/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/{id}',
  method: 'patch',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/{id}',
{
  method: 'PATCH',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.patch '//api.dev.grassrootz.com//api/v2/Organization/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.patch('//api.dev.grassrootz.com//api/v2/Organization/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "//api.dev.grassrootz.com//api/v2/Organization/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v2/Organization/{id}`

*Patches (partial update) an organization object by id*

> Body parameter

```json
[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]
```

<h3 id="apiv2organizationbyidpatch-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the organization object being modified|
|body|body|array[object]|false|The organization model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "currency": "string",
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "fundraisingPageCreatedEmail": "string",
    "id": 0,
    "legalName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "newDonationEmail": "string",
    "newInvoiceEmail": "string",
    "paymentPlatforms": [
      {
        "id": 0,
        "type": "creditCardForm",
        "platform": "stripe"
      }
    ],
    "taxId": "string",
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2organizationbyidpatch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_OrganizationElementModel_](#schemascalaractionresult_organizationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_OrganizationElementModel_](#schemascalaractionresult_organizationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationPublicByUrlPathGet

<a id="opIdApiV2OrganizationPublicByUrlPathGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Organization/public/{urlPath} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Organization/public/{urlPath} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/public/{urlPath}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/public/{urlPath}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Organization/public/{urlPath}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Organization/public/{urlPath}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/public/{urlPath}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Organization/public/{urlPath}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Organization/public/{urlPath}`

*Gets a Organization object by paths*

<h3 id="apiv2organizationpublicbyurlpathget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|urlPath|path|string|true|Organization Url Path|

> Example responses

> 200 Response

```json
{
  "data": {
    "country": "string",
    "currency": "string",
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "id": 0,
    "name": "string",
    "legalName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2organizationpublicbyurlpathget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_OrganizationPublicModel_](#schemascalaractionresult_organizationpublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_OrganizationPublicModel_](#schemascalaractionresult_organizationpublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2OrganizationPost

<a id="opIdApiV2OrganizationPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Organization \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Organization HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization',
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
  "name": "string",
  "mainImagePath": "string",
  "legalName": "string",
  "taxId": "string",
  "urlPath": "string",
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "timezone": "string",
  "adminEmail": "string",
  "fundraisingPageCreatedEmail": "string",
  "newDonationEmail": "string",
  "newInvoiceEmail": "string",
  "template": {
    "key": "string",
    "value": {}
  }
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Organization',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Organization', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Organization", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Organization`

*Creates a new organization*

> Body parameter

```json
{
  "name": "string",
  "mainImagePath": "string",
  "legalName": "string",
  "taxId": "string",
  "urlPath": "string",
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "timezone": "string",
  "adminEmail": "string",
  "fundraisingPageCreatedEmail": "string",
  "newDonationEmail": "string",
  "newInvoiceEmail": "string",
  "template": {
    "key": "string",
    "value": {}
  }
}
```

<h3 id="apiv2organizationpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[OrganizationEditModel](#schemaorganizationeditmodel)|false|The organization model containing the details|

> Example responses

> 201 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "currency": "string",
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "fundraisingPageCreatedEmail": "string",
    "id": 0,
    "legalName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "newDonationEmail": "string",
    "newInvoiceEmail": "string",
    "paymentPlatforms": [
      {
        "id": 0,
        "type": "creditCardForm",
        "platform": "stripe"
      }
    ],
    "taxId": "string",
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2organizationpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_OrganizationElementModel_](#schemascalaractionresult_organizationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_OrganizationElementModel_](#schemascalaractionresult_organizationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationSearchPost

<a id="opIdApiV2OrganizationSearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Organization/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Organization/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Organization/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Organization/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Organization/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Organization/search`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2organizationsearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[OrganizationSearchModel](#schemaorganizationsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "address": {
          "street": "string",
          "city": "string",
          "state": "string",
          "postcode": "string",
          "country": "string"
        },
        "currency": "string",
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "fundraisingPageCreatedEmail": "string",
        "id": 0,
        "legalName": "string",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "newDonationEmail": "string",
        "newInvoiceEmail": "string",
        "paymentPlatforms": [
          {
            "id": 0,
            "type": "creditCardForm",
            "platform": "stripe"
          }
        ],
        "taxId": "string",
        "template": {
          "key": "string",
          "value": {}
        },
        "timezone": "string",
        "urlFull": "string",
        "urlPath": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2organizationsearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_OrganizationElementModel_](#schemalistactionresult_organizationelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_OrganizationElementModel_](#schemalistactionresult_organizationelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationExportPost

<a id="opIdApiV2OrganizationExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Organization/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Organization/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Organization/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Organization/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Organization/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Organization/export`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2organizationexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[OrganizationSearchModel](#schemaorganizationsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2organizationexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationMetadataGet

<a id="opIdApiV2OrganizationMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Organization/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Organization/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Organization/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Organization/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Organization/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Organization/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2organizationmetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationAggregateGet

<a id="opIdApiV2OrganizationAggregateGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Organization/aggregate \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Organization/aggregate HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/aggregate',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/aggregate',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Organization/aggregate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Organization/aggregate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/aggregate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Organization/aggregate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Organization/aggregate`

*Perform an aggregate function on a field based on a filter/custom-text criteria*

<h3 id="apiv2organizationaggregateget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|fieldName|query|string|false|none|
|fieldAggregate|query|string|false|none|
|filters|query|array[any]|false|none|
|text|query|string|false|none|
|orderBy.key|query|string|false|none|
|orderBy.direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|pageSize|query|integer(int32)|false|none|
|resultType|query|string|false|none|
|includeDataTemplate|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|fieldAggregate|sum|
|fieldAggregate|average|
|fieldAggregate|min|
|fieldAggregate|max|
|fieldAggregate|count|
|orderBy.direction|asc|
|orderBy.direction|desc|
|resultType|lookup|
|resultType|basic|
|resultType|full|

> Example responses

> 200 Response

```json
{
  "data": 0,
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2organizationaggregateget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationPaymentPlatformSetupGet

<a id="opIdApiV2OrganizationPaymentPlatformSetupGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Organization/paymentPlatform/setup \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Organization/paymentPlatform/setup HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform/setup',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform/setup',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform/setup',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform/setup', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform/setup");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform/setup", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Organization/paymentPlatform/setup`

*Get a setup link for a payment platform*

<h3 id="apiv2organizationpaymentplatformsetupget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|platform|query|string|false|none|
|organizationId|query|integer(int32)|false|none|
|setupType|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|platform|stripe|
|setupType|oAuth|

> Example responses

> 200 Response

```json
{
  "data": "string",
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2organizationpaymentplatformsetupget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_String_](#schemascalaractionresult_string_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_String_](#schemascalaractionresult_string_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationPaymentPlatformPost

<a id="opIdApiV2OrganizationPaymentPlatformPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Organization/paymentPlatform \
  -H 'Content-Type: application/json-patch+json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Organization/paymentPlatform HTTP/1.1
Host: null
Content-Type: application/json-patch+json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform',
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
  "platform": "stripe",
  "code": "string",
  "state": "string",
  "scope": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform',
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
  'Content-Type' => 'application/json-patch+json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform");
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
        "Content-Type": []string{"application/json-patch+json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Organization/paymentPlatform", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Organization/paymentPlatform`

*Complete payment platform setup*

> Body parameter

```json
{
  "platform": "stripe",
  "code": "string",
  "state": "string",
  "scope": "string"
}
```

<h3 id="apiv2organizationpaymentplatformpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[OrganizationPaymentPlatformEditModel](#schemaorganizationpaymentplatformeditmodel)|false|The model required to complete the setup|

<h3 id="apiv2organizationpaymentplatformpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationWebhookEndpointPost

<a id="opIdApiV2OrganizationWebhookEndpointPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint \
  -H 'Content-Type: application/json-patch+json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint HTTP/1.1
Host: null
Content-Type: application/json-patch+json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint',
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
  "subscriberEndpoint": "string",
  "organizationId": 0
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint',
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
  'Content-Type' => 'application/json-patch+json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint");
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
        "Content-Type": []string{"application/json-patch+json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Organization/webhookEndpoint`

*Setup webhook endpoint*

> Body parameter

```json
{
  "subscriberEndpoint": "string",
  "organizationId": 0
}
```

<h3 id="apiv2organizationwebhookendpointpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[OrganizationWebhookEndpointEditModel](#schemaorganizationwebhookendpointeditmodel)|false|The model required to add the endpoint|

<h3 id="apiv2organizationwebhookendpointpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2OrganizationWebhookEndpointDelete

<a id="opIdApiV2OrganizationWebhookEndpointDelete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE //api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint \
  -H 'Content-Type: application/json-patch+json' \
  -H 'ApiKey: API_KEY'

```

```http
DELETE //api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint HTTP/1.1
Host: null
Content-Type: application/json-patch+json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '0';
const headers = {
  'Content-Type':'application/json-patch+json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint',
{
  method: 'DELETE',
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
  'Content-Type' => 'application/json-patch+json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.delete '//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'ApiKey': 'API_KEY'
}

r = requests.delete('//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Content-Type": []string{"application/json-patch+json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "//api.dev.grassrootz.com//api/v2/Organization/webhookEndpoint", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/Organization/webhookEndpoint`

*Setup webhook endpoint*

> Body parameter

```json
0
```

<h3 id="apiv2organizationwebhookendpointdelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|integer(int32)|false|id of the endpoint|

<h3 id="apiv2organizationwebhookendpointdelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-Page">Page</h1>

## ApiV2PagePublicByPrimaryPathBySecondaryPathByUrlPathGet

<a id="opIdApiV2PagePublicByPrimaryPathBySecondaryPathByUrlPathGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}/{urlPath} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}/{urlPath} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}/{urlPath}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}/{urlPath}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}/{urlPath}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}/{urlPath}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}/{urlPath}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}/{urlPath}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Page/public/{primaryPath}/{secondaryPath}/{urlPath}`

*Gets a fundraiser object by paths*

<h3 id="apiv2pagepublicbyprimarypathbysecondarypathbyurlpathget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|primaryPath|path|string|true|Primary (Event or Organization) Url Path|
|secondaryPath|path|string|true|Secondary (Campaign or Organization) Url Path|
|urlPath|path|string|true|Fundraiser Url Path|

> Example responses

> 201 Response

```json
{
  "data": {
    "type": "organization",
    "campaign": {
      "additionalDonationsNeededForTarget": 0,
      "averageDonationAmount": 0,
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "dataCapture": {
        "registration": {
          "phone": {
            "capture": true,
            "mandatory": true
          },
          "address": {
            "capture": true,
            "mandatory": true
          }
        },
        "donation": {
          "phone": {
            "capture": true,
            "mandatory": true
          },
          "address": {
            "capture": true,
            "mandatory": true
          }
        }
      },
      "donationCount": 0,
      "donationSetup": {
        "allowRecurringGiving": true
      },
      "fundraisersCount": 0,
      "fundraisers": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organizationId": 0,
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "pagesCount": 0,
      "paymentPlatforms": {
        "main": {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        },
        "alternative": [
          {
            "id": 0,
            "platform": "stripe",
            "platformType": "creditCardForm",
            "publicKey": "string"
          }
        ]
      },
      "raisedAmount": 0,
      "targetAmount": 0,
      "type": "default",
      "status": "live",
      "teamsCount": 0,
      "teams": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "fundraiser": {
      "averageDonationAmount": 0,
      "campaign": {
        "allowsFundraisers": true,
        "allowsFundraiserSelfSignUp": true,
        "allowsTeams": true,
        "allowsTeamSelfSignUp": true,
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "id": 0,
      "isPublic": true,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "team": {
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "template": {
        "value": {
          "property1": {},
          "property2": {}
        }
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "organization": {
      "country": "string",
      "currency": "string",
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "id": 0,
      "name": "string",
      "legalName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "timezone": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "team": {
      "averageDonationAmount": 0,
      "campaign": {
        "allowsFundraisers": true,
        "allowsFundraiserSelfSignUp": true,
        "allowsTeams": true,
        "allowsTeamSelfSignUp": true,
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "id": 0,
      "isPublic": true,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "raisedAmount": 0,
      "status": "live",
      "fundraisersCount": 0,
      "targetAmount": 0,
      "template": {
        "value": {
          "property1": {},
          "property2": {}
        }
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagepublicbyprimarypathbysecondarypathbyurlpathget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_PagePublicGeneralModel_](#schemascalaractionresult_pagepublicgeneralmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_PagePublicGeneralModel_](#schemascalaractionresult_pagepublicgeneralmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2PagePublicByPrimaryPathBySecondaryPathGet

<a id="opIdApiV2PagePublicByPrimaryPathBySecondaryPathGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}/{secondaryPath}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Page/public/{primaryPath}/{secondaryPath}`

*Gets a fundraiser object by paths*

<h3 id="apiv2pagepublicbyprimarypathbysecondarypathget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|primaryPath|path|string|true|Primary (Event or Organization) Url Path|
|secondaryPath|path|string|true|Secondary (Campaign or Organization) Url Path|
|urlPath|query|string|false|Fundraiser Url Path|

> Example responses

> 201 Response

```json
{
  "data": {
    "type": "organization",
    "campaign": {
      "additionalDonationsNeededForTarget": 0,
      "averageDonationAmount": 0,
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "dataCapture": {
        "registration": {
          "phone": {
            "capture": true,
            "mandatory": true
          },
          "address": {
            "capture": true,
            "mandatory": true
          }
        },
        "donation": {
          "phone": {
            "capture": true,
            "mandatory": true
          },
          "address": {
            "capture": true,
            "mandatory": true
          }
        }
      },
      "donationCount": 0,
      "donationSetup": {
        "allowRecurringGiving": true
      },
      "fundraisersCount": 0,
      "fundraisers": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organizationId": 0,
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "pagesCount": 0,
      "paymentPlatforms": {
        "main": {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        },
        "alternative": [
          {
            "id": 0,
            "platform": "stripe",
            "platformType": "creditCardForm",
            "publicKey": "string"
          }
        ]
      },
      "raisedAmount": 0,
      "targetAmount": 0,
      "type": "default",
      "status": "live",
      "teamsCount": 0,
      "teams": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "fundraiser": {
      "averageDonationAmount": 0,
      "campaign": {
        "allowsFundraisers": true,
        "allowsFundraiserSelfSignUp": true,
        "allowsTeams": true,
        "allowsTeamSelfSignUp": true,
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "id": 0,
      "isPublic": true,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "team": {
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "template": {
        "value": {
          "property1": {},
          "property2": {}
        }
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "organization": {
      "country": "string",
      "currency": "string",
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "id": 0,
      "name": "string",
      "legalName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "timezone": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "team": {
      "averageDonationAmount": 0,
      "campaign": {
        "allowsFundraisers": true,
        "allowsFundraiserSelfSignUp": true,
        "allowsTeams": true,
        "allowsTeamSelfSignUp": true,
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "id": 0,
      "isPublic": true,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "raisedAmount": 0,
      "status": "live",
      "fundraisersCount": 0,
      "targetAmount": 0,
      "template": {
        "value": {
          "property1": {},
          "property2": {}
        }
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagepublicbyprimarypathbysecondarypathget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_PagePublicGeneralModel_](#schemascalaractionresult_pagepublicgeneralmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_PagePublicGeneralModel_](#schemascalaractionresult_pagepublicgeneralmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2PagePublicByPrimaryPathGet

<a id="opIdApiV2PagePublicByPrimaryPathGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Page/public/{primaryPath} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Page/public/{primaryPath} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Page/public/{primaryPath}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Page/public/{primaryPath}`

*Gets a fundraiser object by paths*

<h3 id="apiv2pagepublicbyprimarypathget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|primaryPath|path|string|true|Primary (Event or Organization) Url Path|
|secondaryPath|query|string|false|Secondary (Campaign or Organization) Url Path|
|urlPath|query|string|false|Fundraiser Url Path|

> Example responses

> 201 Response

```json
{
  "data": {
    "type": "organization",
    "campaign": {
      "additionalDonationsNeededForTarget": 0,
      "averageDonationAmount": 0,
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "dataCapture": {
        "registration": {
          "phone": {
            "capture": true,
            "mandatory": true
          },
          "address": {
            "capture": true,
            "mandatory": true
          }
        },
        "donation": {
          "phone": {
            "capture": true,
            "mandatory": true
          },
          "address": {
            "capture": true,
            "mandatory": true
          }
        }
      },
      "donationCount": 0,
      "donationSetup": {
        "allowRecurringGiving": true
      },
      "fundraisersCount": 0,
      "fundraisers": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organizationId": 0,
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "pagesCount": 0,
      "paymentPlatforms": {
        "main": {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        },
        "alternative": [
          {
            "id": 0,
            "platform": "stripe",
            "platformType": "creditCardForm",
            "publicKey": "string"
          }
        ]
      },
      "raisedAmount": 0,
      "targetAmount": 0,
      "type": "default",
      "status": "live",
      "teamsCount": 0,
      "teams": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "fundraiser": {
      "averageDonationAmount": 0,
      "campaign": {
        "allowsFundraisers": true,
        "allowsFundraiserSelfSignUp": true,
        "allowsTeams": true,
        "allowsTeamSelfSignUp": true,
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "id": 0,
      "isPublic": true,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "team": {
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "template": {
        "value": {
          "property1": {},
          "property2": {}
        }
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "organization": {
      "country": "string",
      "currency": "string",
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "id": 0,
      "name": "string",
      "legalName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "timezone": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "team": {
      "averageDonationAmount": 0,
      "campaign": {
        "allowsFundraisers": true,
        "allowsFundraiserSelfSignUp": true,
        "allowsTeams": true,
        "allowsTeamSelfSignUp": true,
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "id": 0,
      "isPublic": true,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "raisedAmount": 0,
      "status": "live",
      "fundraisersCount": 0,
      "targetAmount": 0,
      "template": {
        "value": {
          "property1": {},
          "property2": {}
        }
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagepublicbyprimarypathget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_PagePublicGeneralModel_](#schemascalaractionresult_pagepublicgeneralmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_PagePublicGeneralModel_](#schemascalaractionresult_pagepublicgeneralmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2PageSearchPost

<a id="opIdApiV2PageSearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Page/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Page/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Page/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Page/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Page/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Page/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Page/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Page/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Page/search`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2pagesearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PageSearchModel](#schemapagesearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "accountId": 0,
        "account": {
          "id": 0,
          "email": "string",
          "firstName": "string",
          "lastName": "string"
        },
        "additionalDonationsNeededForTarget": 0,
        "averageDonationAmount": 0,
        "campaignId": 0,
        "campaign": {
          "name": "string",
          "status": "live",
          "template": {
            "key": "string",
            "value": {}
          },
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "urlPath": "string"
        },
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "donationCount": 0,
        "eventId": 0,
        "event": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "fundraiserId": 0,
        "fundraiser": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "isFundraiserOrTeam": true,
        "isActive": true,
        "isPublic": true,
        "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
        "lastUpdatedAt": "2018-08-20T06:00:18Z",
        "name": "string",
        "newsletterOptIn": true,
        "organizationId": 0,
        "organization": {
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "phoneNumber": "string",
        "raisedAmount": 0,
        "status": "string",
        "targetAmount": 0,
        "teamId": 0,
        "team": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "type": "campaign",
        "urlPath": "string",
        "url": "string",
        "urlFull": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagesearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_PageElementModel_](#schemalistactionresult_pageelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_PageElementModel_](#schemalistactionresult_pageelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageSearchPublicPost

<a id="opIdApiV2PageSearchPublicPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Page/search/public \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Page/search/public HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Page/search/public',
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
  "primaryUrlPath": "string",
  "secondaryUrlPath": "string",
  "tertiaryUrlPath": "string",
  "type": "campaign",
  "isFundraiserOrTeam": true,
  "inactiveOnly": true,
  "text": "string",
  "page": 0,
  "orderKey": "string",
  "orderDirection": "asc"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Page/search/public',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Page/search/public',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Page/search/public', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Page/search/public");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Page/search/public", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Page/search/public`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "primaryUrlPath": "string",
  "secondaryUrlPath": "string",
  "tertiaryUrlPath": "string",
  "type": "campaign",
  "isFundraiserOrTeam": true,
  "inactiveOnly": true,
  "text": "string",
  "page": 0,
  "orderKey": "string",
  "orderDirection": "asc"
}
```

<h3 id="apiv2pagesearchpublicpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PagePublicSearchModel](#schemapagepublicsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "additionalDonationsNeededForTarget": 0,
        "averageDonationAmount": 0,
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "campaignId": 0,
        "campaign": {
          "name": "string",
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "urlPath": "string"
        },
        "donationCount": 0,
        "event": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "fundraiserId": 0,
        "fundraiser": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "name": "string",
        "organizationId": 0,
        "organization": {
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "raisedAmount": 0,
        "status": "string",
        "targetAmount": 0,
        "teamId": 0,
        "team": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "type": "campaign",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagesearchpublicpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_PagePublicModel_](#schemalistactionresult_pagepublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_PagePublicModel_](#schemalistactionresult_pagepublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2PageExportPost

<a id="opIdApiV2PageExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Page/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Page/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Page/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Page/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Page/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Page/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Page/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Page/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Page/export`

*Search (list request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2pageexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[PageSearchModel](#schemapagesearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageMetadataGet

<a id="opIdApiV2PageMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Page/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Page/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Page/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Page/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Page/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Page/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Page/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Page/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Page/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pagemetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageAggregateGet

<a id="opIdApiV2PageAggregateGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Page/aggregate \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Page/aggregate HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Page/aggregate',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Page/aggregate',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Page/aggregate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Page/aggregate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Page/aggregate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Page/aggregate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Page/aggregate`

*Perform an aggregate function on a field based on a filter/custom-text criteria*

<h3 id="apiv2pageaggregateget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|fieldName|query|string|false|none|
|fieldAggregate|query|string|false|none|
|filters|query|array[any]|false|none|
|text|query|string|false|none|
|orderBy.key|query|string|false|none|
|orderBy.direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|pageSize|query|integer(int32)|false|none|
|resultType|query|string|false|none|
|includeDataTemplate|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|fieldAggregate|sum|
|fieldAggregate|average|
|fieldAggregate|min|
|fieldAggregate|max|
|fieldAggregate|count|
|orderBy.direction|asc|
|orderBy.direction|desc|
|resultType|lookup|
|resultType|basic|
|resultType|full|

> Example responses

> 200 Response

```json
{
  "data": 0,
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageaggregateget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-Session">Session</h1>

## ApiV2SessionGet

<a id="opIdApiV2SessionGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/Session \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/Session HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Session',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Session',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/Session',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/Session', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Session");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/Session", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/Session`

*Returns the currently linked session object*

> Example responses

> 200 Response

```json
{
  "data": {
    "key": "string",
    "account": {
      "id": 0,
      "firstName": "string",
      "lastName": "string",
      "source": "default"
    },
    "organization": {
      "id": 0,
      "name": "string"
    },
    "expiry": "2018-08-20T06:00:18Z",
    "impersonated": true,
    "impersonator": {
      "id": 0,
      "firstName": "string",
      "lastName": "string",
      "source": "default"
    },
    "isFundraiser": true,
    "isSystemAdmin": true,
    "isOrganizationAdmin": true,
    "refresh": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2sessionget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_SessionElementModel_](#schemascalaractionresult_sessionelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_SessionElementModel_](#schemascalaractionresult_sessionelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2SessionLoginPost

<a id="opIdApiV2SessionLoginPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Session/login \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Session/login HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Session/login',
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
  "email": "string",
  "password": "string",
  "remember": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Session/login',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Session/login',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Session/login', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Session/login");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Session/login", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Session/login`

*Creates a session through a login procedure, requiring an email and a password*

> Body parameter

```json
{
  "email": "string",
  "password": "string",
  "remember": true
}
```

<h3 id="apiv2sessionloginpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SessionCreateModel](#schemasessioncreatemodel)|false|Model including an email and a password|

> Example responses

> 201 Response

```json
{
  "data": {
    "key": "string",
    "account": {
      "id": 0,
      "firstName": "string",
      "lastName": "string",
      "source": "default"
    },
    "organization": {
      "id": 0,
      "name": "string"
    },
    "expiry": "2018-08-20T06:00:18Z",
    "impersonated": true,
    "impersonator": {
      "id": 0,
      "firstName": "string",
      "lastName": "string",
      "source": "default"
    },
    "isFundraiser": true,
    "isSystemAdmin": true,
    "isOrganizationAdmin": true,
    "refresh": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2sessionloginpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_SessionElementModel_](#schemascalaractionresult_sessionelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_SessionElementModel_](#schemascalaractionresult_sessionelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2SessionFacebookPost

<a id="opIdApiV2SessionFacebookPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Session/facebook \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Session/facebook HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Session/facebook',
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
  "accessCode": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Session/facebook',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Session/facebook',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Session/facebook', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Session/facebook");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Session/facebook", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Session/facebook`

*Initiates a login procedure via a facebook*

> Body parameter

```json
{
  "accessCode": "string"
}
```

<h3 id="apiv2sessionfacebookpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SessionFacebookLoginModel](#schemasessionfacebookloginmodel)|false|Model including an email|

> Example responses

> 201 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2sessionfacebookpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2SessionPasswordlessPost

<a id="opIdApiV2SessionPasswordlessPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Session/passwordless \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Session/passwordless HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Session/passwordless',
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
  "email": "string",
  "returnUrl": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Session/passwordless',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Session/passwordless',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Session/passwordless', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Session/passwordless");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Session/passwordless", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Session/passwordless`

*Initiates a login procedure via a email-magic-link request*

> Body parameter

```json
{
  "email": "string",
  "returnUrl": "string"
}
```

<h3 id="apiv2sessionpasswordlesspost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SessionPasswordLessEditModel](#schemasessionpasswordlesseditmodel)|false|Model including an email|

> Example responses

> 201 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2sessionpasswordlesspost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2SessionActivatePost

<a id="opIdApiV2SessionActivatePost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Session/activate \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Session/activate HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Session/activate',
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
  "id": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Session/activate',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Session/activate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Session/activate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Session/activate");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Session/activate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Session/activate`

*Creates a session through an activate procedure, requiring an activation code*

> Body parameter

```json
{
  "id": "string"
}
```

<h3 id="apiv2sessionactivatepost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SessionActivateEditModel](#schemasessionactivateeditmodel)|false|Model including the activation code|

> Example responses

> 201 Response

```json
{
  "data": {
    "key": "string",
    "account": {
      "id": 0,
      "firstName": "string",
      "lastName": "string",
      "source": "default"
    },
    "organization": {
      "id": 0,
      "name": "string"
    },
    "expiry": "2018-08-20T06:00:18Z",
    "impersonated": true,
    "impersonator": {
      "id": 0,
      "firstName": "string",
      "lastName": "string",
      "source": "default"
    },
    "isFundraiser": true,
    "isSystemAdmin": true,
    "isOrganizationAdmin": true,
    "refresh": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2sessionactivatepost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_SessionElementModel_](#schemascalaractionresult_sessionelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_SessionElementModel_](#schemascalaractionresult_sessionelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2SessionRefreshPost

<a id="opIdApiV2SessionRefreshPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Session/refresh \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Session/refresh HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Session/refresh',
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
  "accountId": 0,
  "code": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Session/refresh',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Session/refresh',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Session/refresh', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Session/refresh");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Session/refresh", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Session/refresh`

*Creates a session through a login procedure, requiring an email and a password*

> Body parameter

```json
{
  "accountId": 0,
  "code": "string"
}
```

<h3 id="apiv2sessionrefreshpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SessionRefreshEditModel](#schemasessionrefresheditmodel)|false|Model including an email and a password|

> Example responses

> 201 Response

```json
{
  "data": {
    "key": "string",
    "account": {
      "id": 0,
      "firstName": "string",
      "lastName": "string",
      "source": "default"
    },
    "organization": {
      "id": 0,
      "name": "string"
    },
    "expiry": "2018-08-20T06:00:18Z",
    "impersonated": true,
    "impersonator": {
      "id": 0,
      "firstName": "string",
      "lastName": "string",
      "source": "default"
    },
    "isFundraiser": true,
    "isSystemAdmin": true,
    "isOrganizationAdmin": true,
    "refresh": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2sessionrefreshpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_SessionElementModel_](#schemascalaractionresult_sessionelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_SessionElementModel_](#schemascalaractionresult_sessionelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2SessionLogoutPost

<a id="opIdApiV2SessionLogoutPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Session/logout \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Session/logout HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Session/logout',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Session/logout',
{
  method: 'POST',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Session/logout',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Session/logout', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Session/logout");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Session/logout", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Session/logout`

*Terminates a session through a logout call*

> Example responses

> 201 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2sessionlogoutpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2SessionImpersonatePost

<a id="opIdApiV2SessionImpersonatePost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/Session/impersonate \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/Session/impersonate HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Session/impersonate',
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
  "accountId": 0
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Session/impersonate',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/Session/impersonate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/Session/impersonate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Session/impersonate");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/Session/impersonate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/Session/impersonate`

*Impersonates the given account using the current admin credential*

> Body parameter

```json
{
  "accountId": 0
}
```

<h3 id="apiv2sessionimpersonatepost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[SessionImpersonateModel](#schemasessionimpersonatemodel)|false|none|

> Example responses

> 201 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2sessionimpersonatepost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2SessionImpersonateDelete

<a id="opIdApiV2SessionImpersonateDelete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE //api.dev.grassrootz.com//api/v2/Session/impersonate \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
DELETE //api.dev.grassrootz.com//api/v2/Session/impersonate HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/Session/impersonate',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/Session/impersonate',
{
  method: 'DELETE',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.delete '//api.dev.grassrootz.com//api/v2/Session/impersonate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.delete('//api.dev.grassrootz.com//api/v2/Session/impersonate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/Session/impersonate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "//api.dev.grassrootz.com//api/v2/Session/impersonate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/Session/impersonate`

*Terminates the impersonation using the current admin credential*

> Example responses

> 201 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2sessionimpersonatedelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-Team">Team</h1>

## ApiV2PageTeamByIdGet

<a id="opIdApiV2PageTeamByIdGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Team/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Team/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Team/{id}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Team/{id}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Team/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Team/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Team/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Team/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Team/{id}`

*Gets a team object by id*

<h3 id="apiv2pageteambyidget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Team id|

> Example responses

> 200 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "averageDonationAmount": 0,
    "campaignId": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "manager": {
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "id": 0
    },
    "name": "string",
    "newsletter": true,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "phoneNumber": "string",
    "raisedAmount": 0,
    "status": "live",
    "fundraisersActiveCount": 0,
    "fundraisersCount": 0,
    "targetAmount": 0,
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageteambyidget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_TeamElementModel_](#schemascalaractionresult_teamelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_TeamElementModel_](#schemascalaractionresult_teamelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageTeamByIdPut

<a id="opIdApiV2PageTeamByIdPut"></a>

> Code samples

```shell
# You can also use wget
curl -X PUT //api.dev.grassrootz.com//api/v2/page/Team/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PUT //api.dev.grassrootz.com//api/v2/page/Team/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Team/{id}',
  method: 'put',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "isPublic": true,
  "mainImagePath": "string",
  "manager": {
    "operation": "unchanged",
    "email": "string",
    "customInviteUrl": "string"
  },
  "name": "string",
  "newsletter": true,
  "phoneNumber": "string",
  "removeAllFundraisers": true,
  "status": "live",
  "targetAmount": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "urlPath": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Team/{id}',
{
  method: 'PUT',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.put '//api.dev.grassrootz.com//api/v2/page/Team/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.put('//api.dev.grassrootz.com//api/v2/page/Team/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Team/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PUT", "//api.dev.grassrootz.com//api/v2/page/Team/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /api/v2/page/Team/{id}`

*Updates a Team object by id*

> Body parameter

```json
{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "isPublic": true,
  "mainImagePath": "string",
  "manager": {
    "operation": "unchanged",
    "email": "string",
    "customInviteUrl": "string"
  },
  "name": "string",
  "newsletter": true,
  "phoneNumber": "string",
  "removeAllFundraisers": true,
  "status": "live",
  "targetAmount": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "urlPath": "string"
}
```

<h3 id="apiv2pageteambyidput-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the team object being modified|
|body|body|[TeamEditModel](#schemateameditmodel)|false|The team model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "averageDonationAmount": 0,
    "campaignId": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "manager": {
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "id": 0
    },
    "name": "string",
    "newsletter": true,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "phoneNumber": "string",
    "raisedAmount": 0,
    "status": "live",
    "fundraisersActiveCount": 0,
    "fundraisersCount": 0,
    "targetAmount": 0,
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageteambyidput-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_TeamElementModel_](#schemascalaractionresult_teamelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_TeamElementModel_](#schemascalaractionresult_teamelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageTeamByIdDelete

<a id="opIdApiV2PageTeamByIdDelete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE //api.dev.grassrootz.com//api/v2/page/Team/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
DELETE //api.dev.grassrootz.com//api/v2/page/Team/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Team/{id}',
  method: 'delete',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Team/{id}',
{
  method: 'DELETE',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.delete '//api.dev.grassrootz.com//api/v2/page/Team/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.delete('//api.dev.grassrootz.com//api/v2/page/Team/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Team/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "//api.dev.grassrootz.com//api/v2/page/Team/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /api/v2/page/Team/{id}`

*Patches (partial update) a team object by id*

<h3 id="apiv2pageteambyiddelete-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the team object being modified|

> Example responses

> 200 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageteambyiddelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ObjectActionResult](#schemaobjectactionresult)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageTeamByIdPatch

<a id="opIdApiV2PageTeamByIdPatch"></a>

> Code samples

```shell
# You can also use wget
curl -X PATCH //api.dev.grassrootz.com//api/v2/page/Team/{id} \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
PATCH //api.dev.grassrootz.com//api/v2/page/Team/{id} HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Team/{id}',
  method: 'patch',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');
const inputBody = '[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Team/{id}',
{
  method: 'PATCH',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.patch '//api.dev.grassrootz.com//api/v2/page/Team/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.patch('//api.dev.grassrootz.com//api/v2/page/Team/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Team/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("PATCH", "//api.dev.grassrootz.com//api/v2/page/Team/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /api/v2/page/Team/{id}`

*Patches (partial update) a team object by id*

> Body parameter

```json
[
  {
    "value": {},
    "path": "string",
    "op": "string",
    "from": "string"
  }
]
```

<h3 id="apiv2pageteambyidpatch-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|The id of the Team object being modified|
|body|body|array[object]|false|The team model containing the changes|

> Example responses

> 200 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "averageDonationAmount": 0,
    "campaignId": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "manager": {
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "id": 0
    },
    "name": "string",
    "newsletter": true,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "phoneNumber": "string",
    "raisedAmount": 0,
    "status": "live",
    "fundraisersActiveCount": 0,
    "fundraisersCount": 0,
    "targetAmount": 0,
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageteambyidpatch-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_TeamElementModel_](#schemascalaractionresult_teamelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_TeamElementModel_](#schemascalaractionresult_teamelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageTeamOwnerByIdHead

<a id="opIdApiV2PageTeamOwnerByIdHead"></a>

> Code samples

```shell
# You can also use wget
curl -X HEAD //api.dev.grassrootz.com//api/v2/page/Team/owner/{id} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
HEAD //api.dev.grassrootz.com//api/v2/page/Team/owner/{id} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Team/owner/{id}',
  method: 'head',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Team/owner/{id}',
{
  method: 'HEAD',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.head '//api.dev.grassrootz.com//api/v2/page/Team/owner/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.head('//api.dev.grassrootz.com//api/v2/page/Team/owner/{id}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Team/owner/{id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("HEAD");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("HEAD", "//api.dev.grassrootz.com//api/v2/page/Team/owner/{id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`HEAD /api/v2/page/Team/owner/{id}`

*Checks a team owner via id*

<h3 id="apiv2pageteamownerbyidhead-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|Team id|

> Example responses

> 200 Response

```json
"string"
```

<h3 id="apiv2pageteamownerbyidhead-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|string|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|string|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageTeamPublicByPrimaryPathBySecondaryPathByUrlPathGet

<a id="opIdApiV2PageTeamPublicByPrimaryPathBySecondaryPathByUrlPathGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Team/public/{primaryPath}/{secondaryPath}/{urlPath} \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Team/public/{primaryPath}/{secondaryPath}/{urlPath} HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Team/public/{primaryPath}/{secondaryPath}/{urlPath}',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Team/public/{primaryPath}/{secondaryPath}/{urlPath}',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Team/public/{primaryPath}/{secondaryPath}/{urlPath}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Team/public/{primaryPath}/{secondaryPath}/{urlPath}', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Team/public/{primaryPath}/{secondaryPath}/{urlPath}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Team/public/{primaryPath}/{secondaryPath}/{urlPath}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Team/public/{primaryPath}/{secondaryPath}/{urlPath}`

*Gets a team object by paths*

<h3 id="apiv2pageteampublicbyprimarypathbysecondarypathbyurlpathget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|primaryPath|path|string|true|Primary (Event or Organization) Url Path|
|secondaryPath|path|string|true|Secondary (Campaign or Organization) Url Path|
|urlPath|path|string|true|Team Url Path|

> Example responses

> 200 Response

```json
{
  "data": {
    "averageDonationAmount": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "raisedAmount": 0,
    "status": "live",
    "fundraisersCount": 0,
    "targetAmount": 0,
    "template": {
      "value": {
        "property1": {},
        "property2": {}
      }
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageteampublicbyprimarypathbysecondarypathbyurlpathget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_TeamPublicModel_](#schemascalaractionresult_teampublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_TeamPublicModel_](#schemascalaractionresult_teampublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader
</aside>

## ApiV2PageTeamPost

<a id="opIdApiV2PageTeamPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Team \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Team HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Team',
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
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "isPublic": true,
  "mainImagePath": "string",
  "manager": {
    "operation": "unchanged",
    "email": "string",
    "customInviteUrl": "string"
  },
  "name": "string",
  "newsletter": true,
  "phoneNumber": "string",
  "removeAllFundraisers": true,
  "status": "live",
  "targetAmount": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "urlPath": "string"
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Team',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Team',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Team', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Team");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Team", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Team`

*Creates a new team*

> Body parameter

```json
{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "isPublic": true,
  "mainImagePath": "string",
  "manager": {
    "operation": "unchanged",
    "email": "string",
    "customInviteUrl": "string"
  },
  "name": "string",
  "newsletter": true,
  "phoneNumber": "string",
  "removeAllFundraisers": true,
  "status": "live",
  "targetAmount": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "urlPath": "string"
}
```

<h3 id="apiv2pageteampost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[TeamEditModel](#schemateameditmodel)|false|The team model containing the details|

> Example responses

> 201 Response

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "averageDonationAmount": 0,
    "campaignId": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "manager": {
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "id": 0
    },
    "name": "string",
    "newsletter": true,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "phoneNumber": "string",
    "raisedAmount": 0,
    "status": "live",
    "fundraisersActiveCount": 0,
    "fundraisersCount": 0,
    "targetAmount": 0,
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageteampost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ScalarActionResult_TeamElementModel_](#schemascalaractionresult_teamelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_TeamElementModel_](#schemascalaractionresult_teamelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageTeamSearchPost

<a id="opIdApiV2PageTeamSearchPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Team/search \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Team/search HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Team/search',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Team/search',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Team/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Team/search', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Team/search");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Team/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Team/search`

*Search (List request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2pageteamsearchpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[TeamSearchModel](#schemateamsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 201 Response

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "address": {
          "street": "string",
          "city": "string",
          "state": "string",
          "postcode": "string",
          "country": "string"
        },
        "averageDonationAmount": 0,
        "campaignId": 0,
        "campaign": {
          "allowsFundraisers": true,
          "allowsFundraiserSelfSignUp": true,
          "allowsTeams": true,
          "allowsTeamSelfSignUp": true,
          "donationCount": 0,
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "raisedAmount": 0,
          "status": "live",
          "targetAmount": 0,
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "donationCount": 0,
        "id": 0,
        "isPublic": true,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "manager": {
          "email": "string",
          "firstName": "string",
          "lastName": "string",
          "id": 0
        },
        "name": "string",
        "newsletter": true,
        "organization": {
          "country": "string",
          "currency": "string",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "phoneNumber": "string",
        "raisedAmount": 0,
        "status": "live",
        "fundraisersActiveCount": 0,
        "fundraisersCount": 0,
        "targetAmount": 0,
        "template": {
          "key": "string",
          "value": {}
        },
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageteamsearchpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success|[ListActionResult_TeamElementModel_](#schemalistactionresult_teamelementmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ListActionResult_TeamElementModel_](#schemalistactionresult_teamelementmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageTeamExportPost

<a id="opIdApiV2PageTeamExportPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/page/Team/export \
  -H 'Content-Type: application/json-patch+json' \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/page/Team/export HTTP/1.1
Host: null
Content-Type: application/json-patch+json
Accept: application/json

```

```javascript
var headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Team/export',
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
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}';
const headers = {
  'Content-Type':'application/json-patch+json',
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Team/export',
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
  'Content-Type' => 'application/json-patch+json',
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/page/Team/export',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json-patch+json',
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/page/Team/export', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Team/export");
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
        "Content-Type": []string{"application/json-patch+json"},
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/page/Team/export", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/page/Team/export`

*Search (List request) of a set of objects based on a list of filters, text, paging and ordering parameters*

> Body parameter

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}
```

<h3 id="apiv2pageteamexportpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[TeamSearchModel](#schemateamsearchmodel)|false|Implements ISearching and offers custom filters, text matching, paging and ordering|

> Example responses

> 400 Response

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageteamexportpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ObjectActionResult](#schemaobjectactionresult)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageTeamMetadataGet

<a id="opIdApiV2PageTeamMetadataGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Team/metadata \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Team/metadata HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Team/metadata',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Team/metadata',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Team/metadata',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Team/metadata', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Team/metadata");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Team/metadata", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Team/metadata`

*Returns a list of filters that can be implemented and work nicely with /search*

> Example responses

> 200 Response

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageteammetadataget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_MetadataPublicModel_](#schemascalaractionresult_metadatapublicmodel_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

## ApiV2PageTeamAggregateGet

<a id="opIdApiV2PageTeamAggregateGet"></a>

> Code samples

```shell
# You can also use wget
curl -X GET //api.dev.grassrootz.com//api/v2/page/Team/aggregate \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
GET //api.dev.grassrootz.com//api/v2/page/Team/aggregate HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/page/Team/aggregate',
  method: 'get',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/page/Team/aggregate',
{
  method: 'GET',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.get '//api.dev.grassrootz.com//api/v2/page/Team/aggregate',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.get('//api.dev.grassrootz.com//api/v2/page/Team/aggregate', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/page/Team/aggregate");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "//api.dev.grassrootz.com//api/v2/page/Team/aggregate", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /api/v2/page/Team/aggregate`

*Perform an aggregate function on a field based on a filter/custom-text criteria*

<h3 id="apiv2pageteamaggregateget-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|fieldName|query|string|false|none|
|fieldAggregate|query|string|false|none|
|filters|query|array[any]|false|none|
|text|query|string|false|none|
|orderBy.key|query|string|false|none|
|orderBy.direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|pageSize|query|integer(int32)|false|none|
|resultType|query|string|false|none|
|includeDataTemplate|query|boolean|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|fieldAggregate|sum|
|fieldAggregate|average|
|fieldAggregate|min|
|fieldAggregate|max|
|fieldAggregate|count|
|orderBy.direction|asc|
|orderBy.direction|desc|
|resultType|lookup|
|resultType|basic|
|resultType|full|

> Example responses

> 200 Response

```json
{
  "data": 0,
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2pageteamaggregateget-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_Decimal_](#schemascalaractionresult_decimal_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

<h1 id="Grassrootz-API-Upload">Upload</h1>

## ApiV2ByEntityByTypeUploadPost

<a id="opIdApiV2ByEntityByTypeUploadPost"></a>

> Code samples

```shell
# You can also use wget
curl -X POST //api.dev.grassrootz.com//api/v2/{entity}/{type}/upload \
  -H 'Accept: application/json' \
  -H 'ApiKey: API_KEY'

```

```http
POST //api.dev.grassrootz.com//api/v2/{entity}/{type}/upload HTTP/1.1
Host: null

Accept: application/json

```

```javascript
var headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

$.ajax({
  url: '//api.dev.grassrootz.com//api/v2/{entity}/{type}/upload',
  method: 'post',

  headers: headers,
  success: function(data) {
    console.log(JSON.stringify(data));
  }
})

```

```javascript--nodejs
const request = require('node-fetch');

const headers = {
  'Accept':'application/json',
  'ApiKey':'API_KEY'

};

fetch('//api.dev.grassrootz.com//api/v2/{entity}/{type}/upload',
{
  method: 'POST',

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
  'Accept' => 'application/json',
  'ApiKey' => 'API_KEY'
}

result = RestClient.post '//api.dev.grassrootz.com//api/v2/{entity}/{type}/upload',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'ApiKey': 'API_KEY'
}

r = requests.post('//api.dev.grassrootz.com//api/v2/{entity}/{type}/upload', params={

}, headers = headers)

print r.json()

```

```java
URL obj = new URL("//api.dev.grassrootz.com//api/v2/{entity}/{type}/upload");
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
        "Accept": []string{"application/json"},
        "ApiKey": []string{"API_KEY"},
        
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "//api.dev.grassrootz.com//api/v2/{entity}/{type}/upload", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /api/v2/{entity}/{type}/upload`

*Uploads a file to online storage and returns the new key for the uploaded file*

<h3 id="apiv2byentitybytypeuploadpost-parameters">Parameters</h3>

|Parameter|In|Type|Required|Description|
|---|---|---|---|---|
|entity|path|string|true|none|
|type|path|string|true|none|
|file|query|string|false|none|
|id|query|integer(int32)|false|none|
|folder|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|entity|organization|
|entity|campaign|
|entity|team|
|entity|fundraiser|
|entity|account|
|entity|event|
|entity|page|
|type|logo|
|type|heroImage|
|type|thankYou|
|type|avatar|
|type|asset|

> Example responses

> 200 Response

```json
{
  "data": "string",
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}
```

<h3 id="apiv2byentitybytypeuploadpost-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success|[ScalarActionResult_String_](#schemascalaractionresult_string_)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Bad Request|[ScalarActionResult_String_](#schemascalaractionresult_string_)|

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
ApiKeyHeader & None
</aside>

# Schemas

<h2 id="tocSaccesskeyelementmodel">AccessKeyElementModel</h2>

<a id="schemaaccesskeyelementmodel"></a>

```json
{
  "organizationId": 0,
  "organization": {
    "id": 0,
    "name": "string",
    "urlPath": "string"
  },
  "clientKey": "string",
  "description": "string",
  "createdAt": "2018-08-20T06:00:18Z"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|organizationId|integer(int32)|false|none|none|
|organization|[AccessKeyOrganizationModel](#schemaaccesskeyorganizationmodel)|false|none|none|
|clientKey|string|false|none|none|
|description|string|false|none|none|
|createdAt|string(date-time)|false|none|none|

<h2 id="tocSerrorresult">ErrorResult</h2>

<a id="schemaerrorresult"></a>

```json
{
  "error": "string",
  "param": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|error|string|false|none|none|
|param|string|false|none|none|

<h2 id="tocSaccesskeyorganizationmodel">AccessKeyOrganizationModel</h2>

<a id="schemaaccesskeyorganizationmodel"></a>

```json
{
  "id": 0,
  "name": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|
|urlPath|string|false|none|none|

<h2 id="tocSaccesskeyeditmodel">AccessKeyEditModel</h2>

<a id="schemaaccesskeyeditmodel"></a>

```json
{
  "organizationId": 0,
  "description": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|organizationId|integer(int32)|false|none|none|
|description|string|false|none|none|

<h2 id="tocSoperation">Operation</h2>

<a id="schemaoperation"></a>

```json
{
  "value": {},
  "path": "string",
  "op": "string",
  "from": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|value|object|false|none|none|
|path|string|false|none|none|
|op|string|false|none|none|
|from|string|false|none|none|

<h2 id="tocSdonationelementmodel">DonationElementModel</h2>

<a id="schemadonationelementmodel"></a>

```json
{
  "accountId": 0,
  "amount": 0,
  "campaignId": 0,
  "campaign": {
    "id": 0,
    "name": "string",
    "urlPath": "string",
    "url": "string",
    "template": {
      "key": "string",
      "value": {}
    }
  },
  "donatedAtLocal": "2018-08-20T06:00:18Z",
  "donatedAt": "2018-08-20T06:00:18Z",
  "donor": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "anonymous": true,
    "businessName": "string",
    "donorId": 0,
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "newsletter": true,
    "phoneNumber": "string"
  },
  "financials": {
    "cardBrand": "string",
    "cardCountry": "string",
    "cardLast4Digits": "string",
    "currency": "string",
    "fee": 0,
    "feeCovered": true,
    "platform": "stripe",
    "refunded": true,
    "refundedAt": "2018-08-20T06:00:18Z",
    "refundedAtLocal": "2018-08-20T06:00:18Z",
    "subscription": true,
    "tax": 0,
    "totalFees": 0,
    "timezone": "string"
  },
  "fundraiserId": 0,
  "fundraiser": {
    "id": 0,
    "name": "string",
    "urlPath": "string",
    "url": "string"
  },
  "id": 0,
  "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
  "lastUpdatedAt": "2018-08-20T06:00:18Z",
  "message": "string",
  "organizationId": 0,
  "organization": {
    "id": 0,
    "name": "string",
    "urlPath": "string"
  },
  "pageType": "campaign",
  "receiptNumber": "string",
  "reply": {
    "displayFirstName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "repliedAtLocal": "2018-08-20T06:00:18Z",
    "repliedAt": "2018-08-20T06:00:18Z",
    "reply": "string"
  },
  "status": "collectedFromCustomer",
  "teamId": 0,
  "team": {
    "id": 0,
    "name": "string",
    "urlPath": "string",
    "url": "string"
  },
  "template": {
    "key": "string",
    "value": {}
  },
  "timezone": "string",
  "type": "online"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|accountId|integer(int32)|false|none|none|
|amount|number(double)|false|none|none|
|campaignId|integer(int32)|false|none|none|
|campaign|[DonationCampaignBasicModel](#schemadonationcampaignbasicmodel)|false|none|none|
|donatedAtLocal|string(date-time)|false|read-only|none|
|donatedAt|string(date-time)|false|none|none|
|donor|[DonationAccountModel](#schemadonationaccountmodel)|false|none|none|
|financials|[DonationFinancialElementModel](#schemadonationfinancialelementmodel)|false|none|none|
|fundraiserId|integer(int32)|false|none|none|
|fundraiser|[DonationFundraiserBasicModel](#schemadonationfundraiserbasicmodel)|false|none|none|
|id|integer(int32)|false|none|none|
|lastUpdatedAtLocal|string(date-time)|false|read-only|none|
|lastUpdatedAt|string(date-time)|false|none|none|
|message|string|false|none|none|
|organizationId|integer(int32)|false|none|none|
|organization|[DonationOrganizationBasicModel](#schemadonationorganizationbasicmodel)|false|none|none|
|pageType|string|false|none|none|
|receiptNumber|string|false|none|none|
|reply|[DonationMessageReplyModel](#schemadonationmessagereplymodel)|false|none|none|
|status|string|false|none|none|
|teamId|integer(int32)|false|none|none|
|team|[DonationTeamBasicModel](#schemadonationteambasicmodel)|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|timezone|string|false|none|none|
|type|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|pageType|campaign|
|pageType|fundraiser|
|pageType|team|
|status|collectedFromCustomer|
|status|inTransitToOrganization|
|status|paidToOrganization|
|status|notPaid|
|type|online|
|type|offline|
|type|pledge|

<h2 id="tocSdonationcampaignbasicmodel">DonationCampaignBasicModel</h2>

<a id="schemadonationcampaignbasicmodel"></a>

```json
{
  "id": 0,
  "name": "string",
  "urlPath": "string",
  "url": "string",
  "template": {
    "key": "string",
    "value": {}
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|
|urlPath|string|false|none|none|
|url|string|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|

<h2 id="tocSdonationaccountmodel">DonationAccountModel</h2>

<a id="schemadonationaccountmodel"></a>

```json
{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "anonymous": true,
  "businessName": "string",
  "donorId": 0,
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "newsletter": true,
  "phoneNumber": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|address|[AddressElementModel](#schemaaddresselementmodel)|false|none|none|
|anonymous|boolean|false|none|none|
|businessName|string|false|none|none|
|donorId|integer(int32)|false|none|none|
|email|string|false|none|none|
|firstName|string|false|none|none|
|lastName|string|false|none|none|
|newsletter|boolean|false|none|none|
|phoneNumber|string|false|none|none|

<h2 id="tocSdonationfinancialelementmodel">DonationFinancialElementModel</h2>

<a id="schemadonationfinancialelementmodel"></a>

```json
{
  "cardBrand": "string",
  "cardCountry": "string",
  "cardLast4Digits": "string",
  "currency": "string",
  "fee": 0,
  "feeCovered": true,
  "platform": "stripe",
  "refunded": true,
  "refundedAt": "2018-08-20T06:00:18Z",
  "refundedAtLocal": "2018-08-20T06:00:18Z",
  "subscription": true,
  "tax": 0,
  "totalFees": 0,
  "timezone": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|cardBrand|string|false|none|none|
|cardCountry|string|false|none|none|
|cardLast4Digits|string|false|none|none|
|currency|string|false|none|none|
|fee|number(double)|false|none|none|
|feeCovered|boolean|false|none|none|
|platform|string|false|none|none|
|refunded|boolean|false|none|none|
|refundedAt|string(date-time)|false|none|none|
|refundedAtLocal|string(date-time)|false|read-only|none|
|subscription|boolean|false|none|none|
|tax|number(double)|false|none|none|
|totalFees|number(double)|false|read-only|none|
|timezone|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|platform|stripe|

<h2 id="tocSdonationfundraiserbasicmodel">DonationFundraiserBasicModel</h2>

<a id="schemadonationfundraiserbasicmodel"></a>

```json
{
  "id": 0,
  "name": "string",
  "urlPath": "string",
  "url": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|
|urlPath|string|false|none|none|
|url|string|false|none|none|

<h2 id="tocSdonationorganizationbasicmodel">DonationOrganizationBasicModel</h2>

<a id="schemadonationorganizationbasicmodel"></a>

```json
{
  "id": 0,
  "name": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|
|urlPath|string|false|none|none|

<h2 id="tocSdonationmessagereplymodel">DonationMessageReplyModel</h2>

<a id="schemadonationmessagereplymodel"></a>

```json
{
  "displayFirstName": "string",
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "repliedAtLocal": "2018-08-20T06:00:18Z",
  "repliedAt": "2018-08-20T06:00:18Z",
  "reply": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|displayFirstName|string|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|repliedAtLocal|string(date-time)|false|read-only|none|
|repliedAt|string(date-time)|false|none|none|
|reply|string|false|none|none|

<h2 id="tocSdonationteambasicmodel">DonationTeamBasicModel</h2>

<a id="schemadonationteambasicmodel"></a>

```json
{
  "id": 0,
  "name": "string",
  "urlPath": "string",
  "url": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|
|urlPath|string|false|none|none|
|url|string|false|none|none|

<h2 id="tocSdatatemplateelementmodel">DataTemplateElementModel</h2>

<a id="schemadatatemplateelementmodel"></a>

```json
{
  "key": "string",
  "value": {}
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|key|string|false|none|none|
|value|object|false|none|none|

<h2 id="tocSaddresselementmodel">AddressElementModel</h2>

<a id="schemaaddresselementmodel"></a>

```json
{
  "street": "string",
  "city": "string",
  "state": "string",
  "postcode": "string",
  "country": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|street|string|false|none|none|
|city|string|false|none|none|
|state|string|false|none|none|
|postcode|string|false|none|none|
|country|string|false|none|none|

<h2 id="tocSobjectactionresult">ObjectActionResult</h2>

<a id="schemaobjectactionresult"></a>

```json
{
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSaccesskeysearchmodel">AccessKeySearchModel</h2>

<a id="schemaaccesskeysearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSlistfilter">ListFilter</h2>

<a id="schemalistfilter"></a>

```json
{
  "key": "string",
  "operator": "equalTo",
  "value": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|key|string|false|none|none|
|operator|string|false|none|none|
|value|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|operator|equalTo|
|operator|greaterThan|
|operator|greaterOrEqualThan|
|operator|lesserThan|
|operator|lesserOrEqualThan|

<h2 id="tocSlistorderby">ListOrderBy</h2>

<a id="schemalistorderby"></a>

```json
{
  "key": "string",
  "direction": "asc"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|key|string|false|none|none|
|direction|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|direction|asc|
|direction|desc|

<h2 id="tocSmetadatapublicmodel">MetadataPublicModel</h2>

<a id="schemametadatapublicmodel"></a>

```json
{
  "columns": [
    {
      "key": "string",
      "dataType": "string",
      "additionalData": {}
    }
  ],
  "filters": [
    "string"
  ],
  "sort": [
    "string"
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|columns|[[ColumnDataPublicModel](#schemacolumndatapublicmodel)]|false|none|none|
|filters|[string]|false|none|none|
|sort|[string]|false|none|none|

<h2 id="tocScolumndatapublicmodel">ColumnDataPublicModel</h2>

<a id="schemacolumndatapublicmodel"></a>

```json
{
  "key": "string",
  "dataType": "string",
  "additionalData": {}
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|key|string|false|none|none|
|dataType|string|false|none|none|
|additionalData|object|false|none|none|

<h2 id="tocSaccountelementmodel">AccountElementModel</h2>

<a id="schemaaccountelementmodel"></a>

```json
{
  "id": 0,
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "createdAt": "2018-08-20T06:00:18Z",
  "lastLoggedInAt": "2018-08-20T06:00:18Z",
  "status": "active",
  "roles": "notDefined",
  "isOrgAdmin": true,
  "isSysAdmin": true,
  "isFundraiser": true,
  "isAdmin": true,
  "organizationId": 0,
  "source": "default",
  "organization": {
    "id": 0,
    "name": "string",
    "urlPath": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|email|string|false|none|none|
|firstName|string|false|none|none|
|lastName|string|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|createdAt|string(date-time)|false|none|none|
|lastLoggedInAt|string(date-time)|false|none|none|
|status|string|false|none|none|
|roles|string|false|none|none|
|isOrgAdmin|boolean|false|none|none|
|isSysAdmin|boolean|false|none|none|
|isFundraiser|boolean|false|none|none|
|isAdmin|boolean|false|read-only|none|
|organizationId|integer(int32)|false|none|none|
|source|string|false|none|none|
|organization|[AccountOrganizationBasicModel](#schemaaccountorganizationbasicmodel)|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|active|
|status|deleted|
|roles|notDefined|
|roles|systemAdmin|
|roles|fundraiser|
|roles|organizationAdmin|
|roles|donor|
|source|default|
|source|facebook|
|source|google|

<h2 id="tocSaccountorganizationbasicmodel">AccountOrganizationBasicModel</h2>

<a id="schemaaccountorganizationbasicmodel"></a>

```json
{
  "id": 0,
  "name": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|
|urlPath|string|false|none|none|

<h2 id="tocSaccounteditmodel">AccountEditModel</h2>

<a id="schemaaccounteditmodel"></a>

```json
{
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "password": "string",
  "mainImagePath": "string",
  "organizationId": 0,
  "roles": "notDefined",
  "asInvite": true,
  "asPublicJoin": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|false|none|none|
|firstName|string|false|none|none|
|lastName|string|false|none|none|
|password|string|false|none|none|
|mainImagePath|string|false|none|none|
|organizationId|integer(int32)|false|none|none|
|roles|string|false|none|none|
|asInvite|boolean|false|none|none|
|asPublicJoin|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|roles|notDefined|
|roles|systemAdmin|
|roles|fundraiser|
|roles|organizationAdmin|
|roles|donor|

<h2 id="tocSaccountpublicmodel">AccountPublicModel</h2>

<a id="schemaaccountpublicmodel"></a>

```json
{
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "sessionKey": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|false|none|none|
|firstName|string|false|none|none|
|lastName|string|false|none|none|
|sessionKey|string|false|none|none|

<h2 id="tocSaccountpasswordresetrequestmodel">AccountPasswordResetRequestModel</h2>

<a id="schemaaccountpasswordresetrequestmodel"></a>

```json
{
  "email": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|false|none|none|

<h2 id="tocSaccountpasswordresetmodel">AccountPasswordResetModel</h2>

<a id="schemaaccountpasswordresetmodel"></a>

```json
{
  "token": "string",
  "newPassword": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|token|string|false|none|none|
|newPassword|string|false|none|none|

<h2 id="tocSaccountsearchmodel">AccountSearchModel</h2>

<a id="schemaaccountsearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSaccountdonorsearchmodel">AccountDonorSearchModel</h2>

<a id="schemaaccountdonorsearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSaccountdonorelementmodel">AccountDonorElementModel</h2>

<a id="schemaaccountdonorelementmodel"></a>

```json
{
  "id": 0,
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "createdAt": "2018-08-20T06:00:18Z",
  "donationCount": 0,
  "raisedAmount": 0,
  "averageDonationAmount": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|email|string|false|none|none|
|firstName|string|false|none|none|
|lastName|string|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|createdAt|string(date-time)|false|none|none|
|donationCount|integer(int32)|false|none|none|
|raisedAmount|number(double)|false|none|none|
|averageDonationAmount|number(double)|false|none|none|

<h2 id="tocSaccountfundraisersearchmodel">AccountFundraiserSearchModel</h2>

<a id="schemaaccountfundraisersearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSaccountfundraiserelementmodel">AccountFundraiserElementModel</h2>

<a id="schemaaccountfundraiserelementmodel"></a>

```json
{
  "id": 0,
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "createdAt": "2018-08-20T06:00:18Z",
  "donationCount": 0,
  "raisedAmount": 0,
  "averageDonationAmount": 0,
  "activePagesCount": 0,
  "pagesCount": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|email|string|false|none|none|
|firstName|string|false|none|none|
|lastName|string|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|createdAt|string(date-time)|false|none|none|
|donationCount|integer(int32)|false|none|none|
|raisedAmount|number(double)|false|none|none|
|averageDonationAmount|number(double)|false|none|none|
|activePagesCount|integer(int32)|false|none|none|
|pagesCount|integer(int32)|false|none|none|

<h2 id="tocScampaignelementmodel">CampaignElementModel</h2>

<a id="schemacampaignelementmodel"></a>

```json
{
  "activePagesCount": 0,
  "additionalDonationsNeededForTarget": 0,
  "averageDonationAmount": 0,
  "createdAtLocal": "2018-08-20T06:00:18Z",
  "createdAt": "2018-08-20T06:00:18Z",
  "dataCapture": {
    "registration": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    },
    "donation": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    }
  },
  "donationCount": 0,
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "fundraisersActiveCount": 0,
  "fundraisersCount": 0,
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "id": 0,
  "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
  "lastUpdatedAtUtc": "2018-08-20T06:00:18Z",
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "organizationId": 0,
  "organization": {
    "country": "string",
    "currency": "string",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "organizationPaymentPlatformId": 0,
  "pagesCount": 0,
  "paymentPlatforms": {
    "main": {
      "id": 0,
      "platform": "stripe",
      "platformType": "creditCardForm",
      "publicKey": "string"
    },
    "alternative": [
      {
        "id": 0,
        "platform": "stripe",
        "platformType": "creditCardForm",
        "publicKey": "string"
      }
    ]
  },
  "raisedAmount": 0,
  "targetAmount": 0,
  "type": "default",
  "status": "live",
  "teamsActiveCount": 0,
  "teamsCount": 0,
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "template": {
    "key": "string",
    "value": {}
  },
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|activePagesCount|integer(int32)|false|none|none|
|additionalDonationsNeededForTarget|number(double)|false|none|none|
|averageDonationAmount|number(double)|false|none|none|
|createdAtLocal|string(date-time)|false|read-only|none|
|createdAt|string(date-time)|false|none|none|
|dataCapture|[FundraisingDataCaptureModel](#schemafundraisingdatacapturemodel)|false|none|none|
|donationCount|integer(int32)|false|none|none|
|donationSetup|[CampaignDonationGeneralModel](#schemacampaigndonationgeneralmodel)|false|none|none|
|fundraisersActiveCount|integer(int32)|false|none|none|
|fundraisersCount|integer(int32)|false|none|none|
|fundraisers|[CampaignFundraiserFundraisingModel](#schemacampaignfundraiserfundraisingmodel)|false|none|none|
|id|integer(int32)|false|none|none|
|lastUpdatedAtLocal|string(date-time)|false|read-only|none|
|lastUpdatedAtUtc|string(date-time)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|organizationId|integer(int32)|false|none|none|
|organization|[CampaignOrganizationModel](#schemacampaignorganizationmodel)|false|none|none|
|organizationPaymentPlatformId|integer(int32)|false|none|none|
|pagesCount|integer(int32)|false|none|none|
|paymentPlatforms|[CampaignPaymentPlatforms_CampaignPaymentPlatformElementModel_](#schemacampaignpaymentplatforms_campaignpaymentplatformelementmodel_)|false|none|none|
|raisedAmount|number(double)|false|none|none|
|targetAmount|number(double)|false|none|none|
|type|string|false|none|none|
|status|string|false|none|none|
|teamsActiveCount|integer(int32)|false|none|none|
|teamsCount|integer(int32)|false|none|none|
|teams|[CampaignTeamFundraisingModel](#schemacampaignteamfundraisingmodel)|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|type|default|
|type|giveNow|
|type|appeal|
|type|bespoke|
|type|inMemory|
|type|celebration|
|type|challenge|
|type|cycling|
|type|running|
|type|event|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSfundraisingdatacapturemodel">FundraisingDataCaptureModel</h2>

<a id="schemafundraisingdatacapturemodel"></a>

```json
{
  "registration": {
    "phone": {
      "capture": true,
      "mandatory": true
    },
    "address": {
      "capture": true,
      "mandatory": true
    }
  },
  "donation": {
    "phone": {
      "capture": true,
      "mandatory": true
    },
    "address": {
      "capture": true,
      "mandatory": true
    }
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|registration|[FundraisingExtraFieldsModel](#schemafundraisingextrafieldsmodel)|false|none|none|
|donation|[FundraisingExtraFieldsModel](#schemafundraisingextrafieldsmodel)|false|none|none|

<h2 id="tocScampaigndonationgeneralmodel">CampaignDonationGeneralModel</h2>

<a id="schemacampaigndonationgeneralmodel"></a>

```json
{
  "allowRecurringGiving": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|allowRecurringGiving|boolean|false|none|none|

<h2 id="tocScampaignfundraiserfundraisingmodel">CampaignFundraiserFundraisingModel</h2>

<a id="schemacampaignfundraiserfundraisingmodel"></a>

```json
{
  "enabled": true,
  "defaultTargetAmount": 0,
  "allowSelfSignUp": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|enabled|boolean|false|none|none|
|defaultTargetAmount|number(double)|false|none|none|
|allowSelfSignUp|boolean|false|none|none|

<h2 id="tocScampaignorganizationmodel">CampaignOrganizationModel</h2>

<a id="schemacampaignorganizationmodel"></a>

```json
{
  "country": "string",
  "currency": "string",
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "template": {
    "key": "string",
    "value": {}
  },
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|country|string|false|none|none|
|currency|string|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

<h2 id="tocScampaignteamfundraisingmodel">CampaignTeamFundraisingModel</h2>

<a id="schemacampaignteamfundraisingmodel"></a>

```json
{
  "enabled": true,
  "defaultTargetAmount": 0,
  "allowSelfSignUp": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|enabled|boolean|false|none|none|
|defaultTargetAmount|number(double)|false|none|none|
|allowSelfSignUp|boolean|false|none|none|

<h2 id="tocSfundraisingextrafieldsmodel">FundraisingExtraFieldsModel</h2>

<a id="schemafundraisingextrafieldsmodel"></a>

```json
{
  "phone": {
    "capture": true,
    "mandatory": true
  },
  "address": {
    "capture": true,
    "mandatory": true
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|phone|[FundraisingFieldModel](#schemafundraisingfieldmodel)|false|none|none|
|address|[FundraisingFieldModel](#schemafundraisingfieldmodel)|false|none|none|

<h2 id="tocScampaignpaymentplatformelementmodel">CampaignPaymentPlatformElementModel</h2>

<a id="schemacampaignpaymentplatformelementmodel"></a>

```json
{
  "id": 0,
  "platform": "stripe",
  "platformType": "creditCardForm",
  "publicKey": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|platform|string|false|none|none|
|platformType|string|false|none|none|
|publicKey|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|platform|stripe|
|platformType|creditCardForm|
|platformType|external|

<h2 id="tocSfundraisingfieldmodel">FundraisingFieldModel</h2>

<a id="schemafundraisingfieldmodel"></a>

```json
{
  "capture": true,
  "mandatory": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|capture|boolean|false|none|none|
|mandatory|boolean|false|none|none|

<h2 id="tocScampaigneditmodel">CampaignEditModel</h2>

<a id="schemacampaigneditmodel"></a>

```json
{
  "fields": {
    "Registration": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Donation": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Ticket": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ]
  },
  "status": "live",
  "targetAmount": 0,
  "organizationId": 0,
  "eventId": 0,
  "organizationPaymentPlatformId": 0,
  "name": "string",
  "mainImagePath": "string",
  "urlPath": "string",
  "type": "default",
  "dataCapture": {
    "registration": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    },
    "donation": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    }
  },
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "template": {
    "key": "string",
    "value": {}
  },
  "additionalPaymentPlatformIds": [
    0
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|fields|object|false|none|none|
|» Registration|[[CustomFieldEditModel](#schemacustomfieldeditmodel)]|false|none|none|
|» Donation|[[CustomFieldEditModel](#schemacustomfieldeditmodel)]|false|none|none|
|» Ticket|[[CustomFieldEditModel](#schemacustomfieldeditmodel)]|false|none|none|
|status|string|false|none|none|
|targetAmount|number(double)|false|none|none|
|organizationId|integer(int32)|false|none|none|
|eventId|integer(int32)|false|none|none|
|organizationPaymentPlatformId|integer(int32)|false|none|none|
|name|string|false|none|none|
|mainImagePath|string|false|none|none|
|urlPath|string|false|none|none|
|type|string|false|none|none|
|dataCapture|[FundraisingDataCaptureEditModel](#schemafundraisingdatacaptureeditmodel)|false|none|none|
|teams|[CampaignFundraisingEditModel](#schemacampaignfundraisingeditmodel)|false|none|none|
|fundraisers|[CampaignFundraisingEditModel](#schemacampaignfundraisingeditmodel)|false|none|none|
|donationSetup|[CampaignDonationGeneralEditModel](#schemacampaigndonationgeneraleditmodel)|false|none|none|
|template|[DataTemplateEditModel](#schemadatatemplateeditmodel)|false|none|none|
|additionalPaymentPlatformIds|[integer]|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|
|type|default|
|type|giveNow|
|type|appeal|
|type|bespoke|
|type|inMemory|
|type|celebration|
|type|challenge|
|type|cycling|
|type|running|
|type|event|

<h2 id="tocScustomfieldeditmodel">CustomFieldEditModel</h2>

<a id="schemacustomfieldeditmodel"></a>

```json
{
  "identifier": "string",
  "type": "text",
  "label": "string",
  "mandatory": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|identifier|string(uuid)|false|none|none|
|type|string|false|none|none|
|label|string|false|none|none|
|mandatory|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|type|text|
|type|date|
|type|multipleChoice|
|type|yesNo|

<h2 id="tocSfundraisingdatacaptureeditmodel">FundraisingDataCaptureEditModel</h2>

<a id="schemafundraisingdatacaptureeditmodel"></a>

```json
{
  "registration": {
    "phone": {
      "capture": true,
      "mandatory": true
    },
    "address": {
      "capture": true,
      "mandatory": true
    }
  },
  "donation": {
    "phone": {
      "capture": true,
      "mandatory": true
    },
    "address": {
      "capture": true,
      "mandatory": true
    }
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|registration|[FundraisingExtraFieldsEditModel](#schemafundraisingextrafieldseditmodel)|false|none|none|
|donation|[FundraisingExtraFieldsEditModel](#schemafundraisingextrafieldseditmodel)|false|none|none|

<h2 id="tocScampaignfundraisingeditmodel">CampaignFundraisingEditModel</h2>

<a id="schemacampaignfundraisingeditmodel"></a>

```json
{
  "enabled": true,
  "defaultTargetAmount": 0,
  "allowSelfSignUp": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|enabled|boolean|false|none|none|
|defaultTargetAmount|number(double)|false|none|none|
|allowSelfSignUp|boolean|false|none|none|

<h2 id="tocScampaigndonationgeneraleditmodel">CampaignDonationGeneralEditModel</h2>

<a id="schemacampaigndonationgeneraleditmodel"></a>

```json
{
  "allowRecurringGiving": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|allowRecurringGiving|boolean|false|none|none|

<h2 id="tocSdatatemplateeditmodel">DataTemplateEditModel</h2>

<a id="schemadatatemplateeditmodel"></a>

```json
{
  "key": "string",
  "value": {}
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|key|string|false|none|none|
|value|object|false|none|none|

<h2 id="tocSfundraisingextrafieldseditmodel">FundraisingExtraFieldsEditModel</h2>

<a id="schemafundraisingextrafieldseditmodel"></a>

```json
{
  "phone": {
    "capture": true,
    "mandatory": true
  },
  "address": {
    "capture": true,
    "mandatory": true
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|phone|[FundraisingFieldEditModel](#schemafundraisingfieldeditmodel)|false|none|none|
|address|[FundraisingFieldEditModel](#schemafundraisingfieldeditmodel)|false|none|none|

<h2 id="tocSfundraisingfieldeditmodel">FundraisingFieldEditModel</h2>

<a id="schemafundraisingfieldeditmodel"></a>

```json
{
  "capture": true,
  "mandatory": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|capture|boolean|false|none|none|
|mandatory|boolean|false|none|none|

<h2 id="tocScampaignpublicmodel">CampaignPublicModel</h2>

<a id="schemacampaignpublicmodel"></a>

```json
{
  "additionalDonationsNeededForTarget": 0,
  "averageDonationAmount": 0,
  "createdAtLocal": "2018-08-20T06:00:18Z",
  "createdAt": "2018-08-20T06:00:18Z",
  "dataCapture": {
    "registration": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    },
    "donation": {
      "phone": {
        "capture": true,
        "mandatory": true
      },
      "address": {
        "capture": true,
        "mandatory": true
      }
    }
  },
  "donationCount": 0,
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "fundraisersCount": 0,
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "organizationId": 0,
  "organization": {
    "country": "string",
    "currency": "string",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "pagesCount": 0,
  "paymentPlatforms": {
    "main": {
      "id": 0,
      "platform": "stripe",
      "platformType": "creditCardForm",
      "publicKey": "string"
    },
    "alternative": [
      {
        "id": 0,
        "platform": "stripe",
        "platformType": "creditCardForm",
        "publicKey": "string"
      }
    ]
  },
  "raisedAmount": 0,
  "targetAmount": 0,
  "type": "default",
  "status": "live",
  "teamsCount": 0,
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "template": {
    "key": "string",
    "value": {}
  },
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|additionalDonationsNeededForTarget|number(double)|false|none|none|
|averageDonationAmount|number(double)|false|none|none|
|createdAtLocal|string(date-time)|false|read-only|none|
|createdAt|string(date-time)|false|none|none|
|dataCapture|[FundraisingDataCaptureModel](#schemafundraisingdatacapturemodel)|false|none|none|
|donationCount|integer(int32)|false|none|none|
|donationSetup|[CampaignDonationGeneralModel](#schemacampaigndonationgeneralmodel)|false|none|none|
|fundraisersCount|integer(int32)|false|none|none|
|fundraisers|[CampaignFundraiserFundraisingModel](#schemacampaignfundraiserfundraisingmodel)|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|organizationId|integer(int32)|false|none|none|
|organization|[CampaignOrganizationPublicModel](#schemacampaignorganizationpublicmodel)|false|none|none|
|pagesCount|integer(int32)|false|none|none|
|paymentPlatforms|[CampaignPaymentPlatforms_CampaignPaymentPlatformElementModel_](#schemacampaignpaymentplatforms_campaignpaymentplatformelementmodel_)|false|none|none|
|raisedAmount|number(double)|false|none|none|
|targetAmount|number(double)|false|none|none|
|type|string|false|none|none|
|status|string|false|none|none|
|teamsCount|integer(int32)|false|none|none|
|teams|[CampaignTeamFundraisingModel](#schemacampaignteamfundraisingmodel)|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|type|default|
|type|giveNow|
|type|appeal|
|type|bespoke|
|type|inMemory|
|type|celebration|
|type|challenge|
|type|cycling|
|type|running|
|type|event|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocScampaignorganizationpublicmodel">CampaignOrganizationPublicModel</h2>

<a id="schemacampaignorganizationpublicmodel"></a>

```json
{
  "country": "string",
  "currency": "string",
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|country|string|false|none|none|
|currency|string|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

<h2 id="tocScampaignsearchmodel">CampaignSearchModel</h2>

<a id="schemacampaignsearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSdonationeditmodel">DonationEditModel</h2>

<a id="schemadonationeditmodel"></a>

```json
{
  "amount": 0,
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "customer": {
    "anonymous": true,
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "businessName": "string",
    "email": "string",
    "firstName": "string",
    "fromCredential": true,
    "lastName": "string",
    "newsletter": true,
    "phoneNumber": "string"
  },
  "fundraiserId": 0,
  "issueReceipt": true,
  "message": "string",
  "payment": {
    "cardBrand": "string",
    "cardCountry": "string",
    "cardExpiryMonth": 0,
    "cardExpiryYear": 0,
    "cardLast4Digits": "stri",
    "coverFee": true,
    "token": "string"
  },
  "teamId": 0,
  "pageType": "campaign",
  "template": {
    "key": "string",
    "value": {}
  },
  "type": "online"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|number(double)|false|none|none|
|campaignId|integer(int32)|false|none|none|
|customFields|[[CustomFieldValueEditModel](#schemacustomfieldvalueeditmodel)]|false|none|none|
|customer|[DonationAccountEditModel](#schemadonationaccounteditmodel)|false|none|none|
|fundraiserId|integer(int32)|false|none|none|
|issueReceipt|boolean|false|none|none|
|message|string|false|none|none|
|payment|[DonationPaymentEditModel](#schemadonationpaymenteditmodel)|false|none|none|
|teamId|integer(int32)|false|none|none|
|pageType|string|false|none|none|
|template|[DataTemplateEditModel](#schemadatatemplateeditmodel)|false|none|none|
|type|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|pageType|campaign|
|pageType|fundraiser|
|pageType|team|
|type|online|
|type|offline|
|type|pledge|

<h2 id="tocScustomfieldvalueeditmodel">CustomFieldValueEditModel</h2>

<a id="schemacustomfieldvalueeditmodel"></a>

```json
{
  "identifier": "string",
  "value": {}
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|identifier|string(uuid)|false|none|none|
|value|object|false|none|none|

<h2 id="tocSdonationaccounteditmodel">DonationAccountEditModel</h2>

<a id="schemadonationaccounteditmodel"></a>

```json
{
  "anonymous": true,
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "businessName": "string",
  "email": "string",
  "firstName": "string",
  "fromCredential": true,
  "lastName": "string",
  "newsletter": true,
  "phoneNumber": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|anonymous|boolean|false|none|none|
|address|[DonationAddressEditModel](#schemadonationaddresseditmodel)|false|none|none|
|businessName|string|false|none|none|
|email|string|false|none|none|
|firstName|string|false|none|none|
|fromCredential|boolean|false|none|none|
|lastName|string|false|none|none|
|newsletter|boolean|false|none|none|
|phoneNumber|string|false|none|none|

<h2 id="tocSdonationpaymenteditmodel">DonationPaymentEditModel</h2>

<a id="schemadonationpaymenteditmodel"></a>

```json
{
  "cardBrand": "string",
  "cardCountry": "string",
  "cardExpiryMonth": 0,
  "cardExpiryYear": 0,
  "cardLast4Digits": "stri",
  "coverFee": true,
  "token": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|cardBrand|string|false|none|none|
|cardCountry|string|false|none|none|
|cardExpiryMonth|integer(int32)|false|none|none|
|cardExpiryYear|integer(int32)|false|none|none|
|cardLast4Digits|string|false|none|none|
|coverFee|boolean|false|none|none|
|token|string|false|none|none|

<h2 id="tocSdonationaddresseditmodel">DonationAddressEditModel</h2>

<a id="schemadonationaddresseditmodel"></a>

```json
{
  "street": "string",
  "city": "string",
  "state": "string",
  "postcode": "string",
  "country": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|street|string|false|none|none|
|city|string|false|none|none|
|state|string|false|none|none|
|postcode|string|false|none|none|
|country|string|false|none|none|

<h2 id="tocSdonationfeecalculationelementmodel">DonationFeeCalculationElementModel</h2>

<a id="schemadonationfeecalculationelementmodel"></a>

```json
{
  "amount": 0,
  "fee": 0,
  "tax": 0,
  "totalFees": 0,
  "totalWithFees": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|number(double)|false|none|none|
|fee|number(double)|false|none|none|
|tax|number(double)|false|none|none|
|totalFees|number(double)|false|read-only|none|
|totalWithFees|number(double)|false|read-only|none|

<h2 id="tocSdonationmessagereplyeditmodel">DonationMessageReplyEditModel</h2>

<a id="schemadonationmessagereplyeditmodel"></a>

```json
{
  "reply": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|reply|string|false|none|none|

<h2 id="tocSdonationsearchmodel">DonationSearchModel</h2>

<a id="schemadonationsearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSdonationpublicsearchmodel">DonationPublicSearchModel</h2>

<a id="schemadonationpublicsearchmodel"></a>

```json
{
  "primaryUrlPath": "string",
  "secondaryUrlPath": "string",
  "tertiaryUrlPath": "string",
  "page": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|primaryUrlPath|string|false|none|none|
|secondaryUrlPath|string|false|none|none|
|tertiaryUrlPath|string|false|none|none|
|page|integer(int32)|false|none|none|

<h2 id="tocSdonationpublicresultmodel">DonationPublicResultModel</h2>

<a id="schemadonationpublicresultmodel"></a>

```json
{
  "amount": 0,
  "anonymous": true,
  "donatedAtLocal": "2018-08-20T06:00:18Z",
  "donatedAt": "2018-08-20T06:00:18Z",
  "donorDisplayName": "string",
  "id": 0,
  "message": "string",
  "pageType": "campaign",
  "reply": {
    "displayFirstName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "repliedAtLocal": "2018-08-20T06:00:18Z",
    "repliedAt": "2018-08-20T06:00:18Z",
    "reply": "string"
  },
  "type": "online"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|number(double)|false|none|none|
|anonymous|boolean|false|none|none|
|donatedAtLocal|string(date-time)|false|read-only|none|
|donatedAt|string(date-time)|false|none|none|
|donorDisplayName|string|false|none|none|
|id|integer(int32)|false|none|none|
|message|string|false|none|none|
|pageType|string|false|none|none|
|reply|[DonationMessageReplyModel](#schemadonationmessagereplymodel)|false|none|none|
|type|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|pageType|campaign|
|pageType|fundraiser|
|pageType|team|
|type|online|
|type|offline|
|type|pledge|

<h2 id="tocSdonationfeeelementmodel">DonationFeeElementModel</h2>

<a id="schemadonationfeeelementmodel"></a>

```json
{
  "organizationId": 0,
  "organization": {
    "id": 0,
    "name": "string"
  },
  "eventId": 0,
  "event": {
    "id": 0,
    "name": "string"
  },
  "campaignId": 0,
  "campaign": {
    "id": 0,
    "name": "string"
  },
  "fee": 0,
  "feeType": "flatPercentage"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|organizationId|integer(int32)|false|none|none|
|organization|[DonationFeeOrganizationModel](#schemadonationfeeorganizationmodel)|false|none|none|
|eventId|integer(int32)|false|none|none|
|event|[DonationFeeEventModel](#schemadonationfeeeventmodel)|false|none|none|
|campaignId|integer(int32)|false|none|none|
|campaign|[DonationFeeCampaignModel](#schemadonationfeecampaignmodel)|false|none|none|
|fee|number(double)|false|none|none|
|feeType|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|feeType|flatPercentage|

<h2 id="tocSdonationfeeorganizationmodel">DonationFeeOrganizationModel</h2>

<a id="schemadonationfeeorganizationmodel"></a>

```json
{
  "id": 0,
  "name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|

<h2 id="tocSdonationfeeeventmodel">DonationFeeEventModel</h2>

<a id="schemadonationfeeeventmodel"></a>

```json
{
  "id": 0,
  "name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|

<h2 id="tocSdonationfeecampaignmodel">DonationFeeCampaignModel</h2>

<a id="schemadonationfeecampaignmodel"></a>

```json
{
  "id": 0,
  "name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|

<h2 id="tocSdonationfeeeditmodel">DonationFeeEditModel</h2>

<a id="schemadonationfeeeditmodel"></a>

```json
{
  "organizationId": 0,
  "campaignId": 0,
  "eventId": 0,
  "fee": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|organizationId|integer(int32)|false|none|none|
|campaignId|integer(int32)|false|none|none|
|eventId|integer(int32)|false|none|none|
|fee|number(double)|false|none|none|

<h2 id="tocSdonationfeesearchmodel">DonationFeeSearchModel</h2>

<a id="schemadonationfeesearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSeventelementmodel">EventElementModel</h2>

<a id="schemaeventelementmodel"></a>

```json
{
  "id": 0,
  "organizationId": 0,
  "organizationFee": 0,
  "name": "string",
  "createdAt": "2018-08-20T06:00:18Z",
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "urlPath": "string",
  "status": "live",
  "targetAmount": 0,
  "averageDonationAmount": 0,
  "raisedAmount": 0,
  "donationCount": 0,
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "organizations": [
    {
      "id": 0,
      "name": "string",
      "priority": "Tertiary"
    }
  ],
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "fields": {
    "Registration": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Donation": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Ticket": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ]
  },
  "template": {
    "key": "string",
    "value": {}
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|organizationId|integer(int32)|false|none|none|
|organizationFee|number(double)|false|none|none|
|name|string|false|none|none|
|createdAt|string(date-time)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|urlPath|string|false|none|none|
|status|string|false|none|none|
|targetAmount|number(double)|false|none|none|
|averageDonationAmount|number(double)|false|none|none|
|raisedAmount|number(double)|false|none|none|
|donationCount|integer(int32)|false|none|none|
|donationSetup|[EventDonationGeneralModel](#schemaeventdonationgeneralmodel)|false|none|none|
|organizations|[[EventOrganizationModel](#schemaeventorganizationmodel)]|false|none|none|
|fundraisers|[EventFundraisingModel](#schemaeventfundraisingmodel)|false|none|none|
|teams|[EventFundraisingModel](#schemaeventfundraisingmodel)|false|none|none|
|fields|object|false|none|none|
|» Registration|[[CustomFieldEditModel](#schemacustomfieldeditmodel)]|false|none|none|
|» Donation|[[CustomFieldEditModel](#schemacustomfieldeditmodel)]|false|none|none|
|» Ticket|[[CustomFieldEditModel](#schemacustomfieldeditmodel)]|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSeventdonationgeneralmodel">EventDonationGeneralModel</h2>

<a id="schemaeventdonationgeneralmodel"></a>

```json
{
  "allowRecurringGiving": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|allowRecurringGiving|boolean|false|none|none|

<h2 id="tocSeventorganizationmodel">EventOrganizationModel</h2>

<a id="schemaeventorganizationmodel"></a>

```json
{
  "id": 0,
  "name": "string",
  "priority": "Tertiary"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|
|priority|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|priority|Tertiary|
|priority|Secondary|
|priority|Primary|

<h2 id="tocSeventfundraisingmodel">EventFundraisingModel</h2>

<a id="schemaeventfundraisingmodel"></a>

```json
{
  "enabled": true,
  "defaultTargetAmount": 0,
  "allowSelfSignUp": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|enabled|boolean|false|none|none|
|defaultTargetAmount|number(double)|false|none|none|
|allowSelfSignUp|boolean|false|none|none|

<h2 id="tocSeventeditmodel">EventEditModel</h2>

<a id="schemaeventeditmodel"></a>

```json
{
  "organizationId": 0,
  "organizationFee": 0,
  "name": "string",
  "mainImagePath": "string",
  "urlPath": "string",
  "status": "live",
  "targetAmount": 0,
  "fields": {
    "Registration": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Donation": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ],
    "Ticket": [
      {
        "identifier": "string",
        "type": "text",
        "label": "string",
        "mandatory": true
      }
    ]
  },
  "organizations": [
    {
      "id": 0,
      "priority": "Tertiary"
    }
  ],
  "donationSetup": {
    "allowRecurringGiving": true
  },
  "fundraisers": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "teams": {
    "enabled": true,
    "defaultTargetAmount": 0,
    "allowSelfSignUp": true
  },
  "external": {
    "system": "active",
    "registrationUrl": "string",
    "id": "string"
  },
  "template": {
    "key": "string",
    "value": {}
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|organizationId|integer(int32)|false|none|none|
|organizationFee|number(double)|false|none|none|
|name|string|false|none|none|
|mainImagePath|string|false|none|none|
|urlPath|string|false|none|none|
|status|string|false|none|none|
|targetAmount|number(double)|false|none|none|
|fields|object|false|none|none|
|» Registration|[[CustomFieldEditModel](#schemacustomfieldeditmodel)]|false|none|none|
|» Donation|[[CustomFieldEditModel](#schemacustomfieldeditmodel)]|false|none|none|
|» Ticket|[[CustomFieldEditModel](#schemacustomfieldeditmodel)]|false|none|none|
|organizations|[[EventOrganizationEditModel](#schemaeventorganizationeditmodel)]|false|none|none|
|donationSetup|[EventDonationGeneralEditModel](#schemaeventdonationgeneraleditmodel)|false|none|none|
|fundraisers|[EventFundraisingEditModel](#schemaeventfundraisingeditmodel)|false|none|none|
|teams|[EventFundraisingEditModel](#schemaeventfundraisingeditmodel)|false|none|none|
|external|[EventExternalEditModel](#schemaeventexternaleditmodel)|false|none|none|
|template|[DataTemplateEditModel](#schemadatatemplateeditmodel)|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSeventorganizationeditmodel">EventOrganizationEditModel</h2>

<a id="schemaeventorganizationeditmodel"></a>

```json
{
  "id": 0,
  "priority": "Tertiary"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|priority|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|priority|Tertiary|
|priority|Secondary|
|priority|Primary|

<h2 id="tocSeventdonationgeneraleditmodel">EventDonationGeneralEditModel</h2>

<a id="schemaeventdonationgeneraleditmodel"></a>

```json
{
  "allowRecurringGiving": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|allowRecurringGiving|boolean|false|none|none|

<h2 id="tocSeventfundraisingeditmodel">EventFundraisingEditModel</h2>

<a id="schemaeventfundraisingeditmodel"></a>

```json
{
  "enabled": true,
  "defaultTargetAmount": 0,
  "allowSelfSignUp": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|enabled|boolean|false|none|none|
|defaultTargetAmount|number(double)|false|none|none|
|allowSelfSignUp|boolean|false|none|none|

<h2 id="tocSeventexternaleditmodel">EventExternalEditModel</h2>

<a id="schemaeventexternaleditmodel"></a>

```json
{
  "system": "active",
  "registrationUrl": "string",
  "id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|system|string|false|none|none|
|registrationUrl|string|false|none|none|
|id|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|system|active|
|system|tiktok|

<h2 id="tocSeventsearchmodel">EventSearchModel</h2>

<a id="schemaeventsearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSfundraiserelementmodel">FundraiserElementModel</h2>

<a id="schemafundraiserelementmodel"></a>

```json
{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "averageDonationAmount": 0,
  "campaignId": 0,
  "campaign": {
    "allowsFundraisers": true,
    "allowsFundraiserSelfSignUp": true,
    "allowsTeams": true,
    "allowsTeamSelfSignUp": true,
    "donationCount": 0,
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "createdAtLocal": "2018-08-20T06:00:18Z",
  "createdAt": "2018-08-20T06:00:18Z",
  "donationCount": 0,
  "id": 0,
  "isPublic": true,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "manager": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "id": 0
  },
  "name": "string",
  "newsletter": true,
  "organization": {
    "country": "string",
    "currency": "string",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "phoneNumber": "string",
  "raisedAmount": 0,
  "status": "live",
  "targetAmount": 0,
  "teamId": 0,
  "team": {
    "donationCount": 0,
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "raisedAmount": 0,
    "targetAmount": 0,
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "template": {
    "key": "string",
    "value": {}
  },
  "urlPath": "string",
  "url": "string",
  "urlFull": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|address|[FundraiserAddressModel](#schemafundraiseraddressmodel)|false|none|none|
|averageDonationAmount|number(double)|false|none|none|
|campaignId|integer(int32)|false|none|none|
|campaign|[FundraiserCampaignModel](#schemafundraisercampaignmodel)|false|none|none|
|createdAtLocal|string(date-time)|false|read-only|none|
|createdAt|string(date-time)|false|none|none|
|donationCount|integer(int32)|false|none|none|
|id|integer(int32)|false|none|none|
|isPublic|boolean|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|manager|[FundraiserManagerModel](#schemafundraisermanagermodel)|false|none|none|
|name|string|false|none|none|
|newsletter|boolean|false|none|none|
|organization|[FundraiserOrganizationModel](#schemafundraiserorganizationmodel)|false|none|none|
|phoneNumber|string|false|none|none|
|raisedAmount|number(double)|false|none|none|
|status|string|false|none|none|
|targetAmount|number(double)|false|none|none|
|teamId|integer(int32)|false|none|none|
|team|[FundraiserTeamModel](#schemafundraiserteammodel)|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|urlPath|string|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSfundraiseraddressmodel">FundraiserAddressModel</h2>

<a id="schemafundraiseraddressmodel"></a>

```json
{
  "street": "string",
  "city": "string",
  "state": "string",
  "postcode": "string",
  "country": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|street|string|false|none|none|
|city|string|false|none|none|
|state|string|false|none|none|
|postcode|string|false|none|none|
|country|string|false|none|none|

<h2 id="tocSfundraisercampaignmodel">FundraiserCampaignModel</h2>

<a id="schemafundraisercampaignmodel"></a>

```json
{
  "allowsFundraisers": true,
  "allowsFundraiserSelfSignUp": true,
  "allowsTeams": true,
  "allowsTeamSelfSignUp": true,
  "donationCount": 0,
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "raisedAmount": 0,
  "status": "live",
  "targetAmount": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|allowsFundraisers|boolean|false|none|none|
|allowsFundraiserSelfSignUp|boolean|false|none|none|
|allowsTeams|boolean|false|none|none|
|allowsTeamSelfSignUp|boolean|false|none|none|
|donationCount|integer(int32)|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|raisedAmount|number(double)|false|none|none|
|status|string|false|none|none|
|targetAmount|number(double)|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSfundraisermanagermodel">FundraiserManagerModel</h2>

<a id="schemafundraisermanagermodel"></a>

```json
{
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "id": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|false|none|none|
|firstName|string|false|none|none|
|lastName|string|false|none|none|
|id|integer(int32)|false|none|none|

<h2 id="tocSfundraiserorganizationmodel">FundraiserOrganizationModel</h2>

<a id="schemafundraiserorganizationmodel"></a>

```json
{
  "country": "string",
  "currency": "string",
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "template": {
    "key": "string",
    "value": {}
  },
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|country|string|false|none|none|
|currency|string|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

<h2 id="tocSfundraiserteammodel">FundraiserTeamModel</h2>

<a id="schemafundraiserteammodel"></a>

```json
{
  "donationCount": 0,
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "raisedAmount": 0,
  "targetAmount": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|donationCount|integer(int32)|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|raisedAmount|number(double)|false|none|none|
|targetAmount|number(double)|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

<h2 id="tocSfundraisereditmodel">FundraiserEditModel</h2>

<a id="schemafundraisereditmodel"></a>

```json
{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "isPublic": true,
  "mainImagePath": "string",
  "manager": {
    "operation": "unchanged",
    "email": "string",
    "customInviteUrl": "string"
  },
  "name": "string",
  "newsletter": true,
  "phoneNumber": "string",
  "status": "live",
  "targetAmount": 0,
  "teamId": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|address|[FundraiserAddressEditModel](#schemafundraiseraddresseditmodel)|false|none|none|
|campaignId|integer(int32)|false|none|none|
|customFields|[[CustomFieldValueEditModel](#schemacustomfieldvalueeditmodel)]|false|none|none|
|isPublic|boolean|false|none|none|
|mainImagePath|string|false|none|none|
|manager|[FundraiserManagerEditModel](#schemafundraisermanagereditmodel)|false|none|none|
|name|string|false|none|none|
|newsletter|boolean|false|none|none|
|phoneNumber|string|false|none|none|
|status|string|false|none|none|
|targetAmount|number(double)|false|none|none|
|teamId|integer(int32)|false|none|none|
|template|[DataTemplateEditModel](#schemadatatemplateeditmodel)|false|none|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSfundraiseraddresseditmodel">FundraiserAddressEditModel</h2>

<a id="schemafundraiseraddresseditmodel"></a>

```json
{
  "street": "string",
  "city": "string",
  "state": "string",
  "postcode": "string",
  "country": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|street|string|false|none|none|
|city|string|false|none|none|
|state|string|false|none|none|
|postcode|string|false|none|none|
|country|string|false|none|none|

<h2 id="tocSfundraisermanagereditmodel">FundraiserManagerEditModel</h2>

<a id="schemafundraisermanagereditmodel"></a>

```json
{
  "operation": "unchanged",
  "email": "string",
  "customInviteUrl": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|operation|string|false|none|none|
|email|string|false|none|none|
|customInviteUrl|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|operation|unchanged|
|operation|remove|
|operation|new|
|operation|fromCredential|

<h2 id="tocSfundraiserpublicmodel">FundraiserPublicModel</h2>

<a id="schemafundraiserpublicmodel"></a>

```json
{
  "averageDonationAmount": 0,
  "campaign": {
    "allowsFundraisers": true,
    "allowsFundraiserSelfSignUp": true,
    "allowsTeams": true,
    "allowsTeamSelfSignUp": true,
    "donationCount": 0,
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "createdAtLocal": "2018-08-20T06:00:18Z",
  "createdAt": "2018-08-20T06:00:18Z",
  "donationCount": 0,
  "id": 0,
  "isPublic": true,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "organization": {
    "country": "string",
    "currency": "string",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "raisedAmount": 0,
  "status": "live",
  "targetAmount": 0,
  "team": {
    "donationCount": 0,
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "raisedAmount": 0,
    "targetAmount": 0,
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "template": {
    "value": {
      "property1": {},
      "property2": {}
    }
  },
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|averageDonationAmount|number(double)|false|none|none|
|campaign|[FundraiserCampaignPublicModel](#schemafundraisercampaignpublicmodel)|false|none|none|
|createdAtLocal|string(date-time)|false|read-only|none|
|createdAt|string(date-time)|false|none|none|
|donationCount|integer(int32)|false|none|none|
|id|integer(int32)|false|none|none|
|isPublic|boolean|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|organization|[FundraiserOrganizationPublicModel](#schemafundraiserorganizationpublicmodel)|false|none|none|
|raisedAmount|number(double)|false|none|none|
|status|string|false|none|none|
|targetAmount|number(double)|false|none|none|
|team|[FundraiserTeamPublicModel](#schemafundraiserteampublicmodel)|false|none|none|
|template|[DataTemplatePublicModel](#schemadatatemplatepublicmodel)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSfundraisercampaignpublicmodel">FundraiserCampaignPublicModel</h2>

<a id="schemafundraisercampaignpublicmodel"></a>

```json
{
  "allowsFundraisers": true,
  "allowsFundraiserSelfSignUp": true,
  "allowsTeams": true,
  "allowsTeamSelfSignUp": true,
  "donationCount": 0,
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "raisedAmount": 0,
  "status": "live",
  "targetAmount": 0,
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|allowsFundraisers|boolean|false|none|none|
|allowsFundraiserSelfSignUp|boolean|false|none|none|
|allowsTeams|boolean|false|none|none|
|allowsTeamSelfSignUp|boolean|false|none|none|
|donationCount|integer(int32)|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|raisedAmount|number(double)|false|none|none|
|status|string|false|none|none|
|targetAmount|number(double)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSfundraiserorganizationpublicmodel">FundraiserOrganizationPublicModel</h2>

<a id="schemafundraiserorganizationpublicmodel"></a>

```json
{
  "country": "string",
  "currency": "string",
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|country|string|false|none|none|
|currency|string|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

<h2 id="tocSfundraiserteampublicmodel">FundraiserTeamPublicModel</h2>

<a id="schemafundraiserteampublicmodel"></a>

```json
{
  "donationCount": 0,
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "raisedAmount": 0,
  "targetAmount": 0,
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|donationCount|integer(int32)|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|raisedAmount|number(double)|false|none|none|
|targetAmount|number(double)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

<h2 id="tocSdatatemplatepublicmodel">DataTemplatePublicModel</h2>

<a id="schemadatatemplatepublicmodel"></a>

```json
{
  "value": {
    "property1": {},
    "property2": {}
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|value|object|false|none|none|
|» **additionalProperties**|object|false|none|none|

<h2 id="tocSfundraisersearchmodel">FundraiserSearchModel</h2>

<a id="schemafundraisersearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSorganizationelementmodel">OrganizationElementModel</h2>

<a id="schemaorganizationelementmodel"></a>

```json
{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "currency": "string",
  "createdAtLocal": "2018-08-20T06:00:18Z",
  "createdAt": "2018-08-20T06:00:18Z",
  "fundraisingPageCreatedEmail": "string",
  "id": 0,
  "legalName": "string",
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "newDonationEmail": "string",
  "newInvoiceEmail": "string",
  "paymentPlatforms": [
    {
      "id": 0,
      "type": "creditCardForm",
      "platform": "stripe"
    }
  ],
  "taxId": "string",
  "template": {
    "key": "string",
    "value": {}
  },
  "timezone": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|address|[OrganizationAddressModel](#schemaorganizationaddressmodel)|false|none|none|
|currency|string|false|none|none|
|createdAtLocal|string(date-time)|false|read-only|none|
|createdAt|string(date-time)|false|none|none|
|fundraisingPageCreatedEmail|string|false|none|none|
|id|integer(int32)|false|none|none|
|legalName|string|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|newDonationEmail|string|false|none|none|
|newInvoiceEmail|string|false|none|none|
|paymentPlatforms|[[OrganizationPaymentPlatformModel](#schemaorganizationpaymentplatformmodel)]|false|none|none|
|taxId|string|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|timezone|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

<h2 id="tocSorganizationaddressmodel">OrganizationAddressModel</h2>

<a id="schemaorganizationaddressmodel"></a>

```json
{
  "street": "string",
  "city": "string",
  "state": "string",
  "postcode": "string",
  "country": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|street|string|false|none|none|
|city|string|false|none|none|
|state|string|false|none|none|
|postcode|string|false|none|none|
|country|string|false|none|none|

<h2 id="tocSorganizationpaymentplatformmodel">OrganizationPaymentPlatformModel</h2>

<a id="schemaorganizationpaymentplatformmodel"></a>

```json
{
  "id": 0,
  "type": "creditCardForm",
  "platform": "stripe"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|type|string|false|none|none|
|platform|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|type|creditCardForm|
|type|external|
|platform|stripe|

<h2 id="tocSorganizationeditmodel">OrganizationEditModel</h2>

<a id="schemaorganizationeditmodel"></a>

```json
{
  "name": "string",
  "mainImagePath": "string",
  "legalName": "string",
  "taxId": "string",
  "urlPath": "string",
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "timezone": "string",
  "adminEmail": "string",
  "fundraisingPageCreatedEmail": "string",
  "newDonationEmail": "string",
  "newInvoiceEmail": "string",
  "template": {
    "key": "string",
    "value": {}
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|false|none|none|
|mainImagePath|string|false|none|none|
|legalName|string|false|none|none|
|taxId|string|false|none|none|
|urlPath|string|false|none|none|
|address|[OrganizationAddressEditModel](#schemaorganizationaddresseditmodel)|false|none|none|
|timezone|string|false|none|none|
|adminEmail|string|false|none|none|
|fundraisingPageCreatedEmail|string|false|none|none|
|newDonationEmail|string|false|none|none|
|newInvoiceEmail|string|false|none|none|
|template|[DataTemplateEditModel](#schemadatatemplateeditmodel)|false|none|none|

<h2 id="tocSorganizationaddresseditmodel">OrganizationAddressEditModel</h2>

<a id="schemaorganizationaddresseditmodel"></a>

```json
{
  "street": "string",
  "city": "string",
  "state": "string",
  "postcode": "string",
  "country": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|street|string|false|none|none|
|city|string|false|none|none|
|state|string|false|none|none|
|postcode|string|false|none|none|
|country|string|false|none|none|

<h2 id="tocSorganizationpublicmodel">OrganizationPublicModel</h2>

<a id="schemaorganizationpublicmodel"></a>

```json
{
  "country": "string",
  "currency": "string",
  "createdAtLocal": "2018-08-20T06:00:18Z",
  "createdAt": "2018-08-20T06:00:18Z",
  "id": 0,
  "name": "string",
  "legalName": "string",
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "template": {
    "key": "string",
    "value": {}
  },
  "timezone": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|country|string|false|none|none|
|currency|string|false|none|none|
|createdAtLocal|string(date-time)|false|read-only|none|
|createdAt|string(date-time)|false|none|none|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|
|legalName|string|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|timezone|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

<h2 id="tocSorganizationsearchmodel">OrganizationSearchModel</h2>

<a id="schemaorganizationsearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSorganizationpaymentplatformeditmodel">OrganizationPaymentPlatformEditModel</h2>

<a id="schemaorganizationpaymentplatformeditmodel"></a>

```json
{
  "platform": "stripe",
  "code": "string",
  "state": "string",
  "scope": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|platform|string|false|none|none|
|code|string|false|none|none|
|state|string(uuid)|false|none|none|
|scope|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|platform|stripe|

<h2 id="tocSorganizationwebhookendpointeditmodel">OrganizationWebhookEndpointEditModel</h2>

<a id="schemaorganizationwebhookendpointeditmodel"></a>

```json
{
  "subscriberEndpoint": "string",
  "organizationId": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|subscriberEndpoint|string|false|none|none|
|organizationId|integer(int32)|false|none|none|

<h2 id="tocSpagepublicgeneralmodel">PagePublicGeneralModel</h2>

<a id="schemapagepublicgeneralmodel"></a>

```json
{
  "type": "organization",
  "campaign": {
    "additionalDonationsNeededForTarget": 0,
    "averageDonationAmount": 0,
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "dataCapture": {
      "registration": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      },
      "donation": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      }
    },
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "fundraisersCount": 0,
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organizationId": 0,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "pagesCount": 0,
    "paymentPlatforms": {
      "main": {
        "id": 0,
        "platform": "stripe",
        "platformType": "creditCardForm",
        "publicKey": "string"
      },
      "alternative": [
        {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        }
      ]
    },
    "raisedAmount": 0,
    "targetAmount": 0,
    "type": "default",
    "status": "live",
    "teamsCount": 0,
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "fundraiser": {
    "averageDonationAmount": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "team": {
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "targetAmount": 0,
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "template": {
      "value": {
        "property1": {},
        "property2": {}
      }
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "organization": {
    "country": "string",
    "currency": "string",
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "id": 0,
    "name": "string",
    "legalName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "team": {
    "averageDonationAmount": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "raisedAmount": 0,
    "status": "live",
    "fundraisersCount": 0,
    "targetAmount": 0,
    "template": {
      "value": {
        "property1": {},
        "property2": {}
      }
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|type|string|false|read-only|none|
|campaign|[CampaignPublicModel](#schemacampaignpublicmodel)|false|none|none|
|fundraiser|[FundraiserPublicModel](#schemafundraiserpublicmodel)|false|none|none|
|organization|[OrganizationPublicModel](#schemaorganizationpublicmodel)|false|none|none|
|team|[TeamPublicModel](#schemateampublicmodel)|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|type|organization|
|type|campaign|
|type|event|
|type|fundraiser|
|type|team|

<h2 id="tocSteampublicmodel">TeamPublicModel</h2>

<a id="schemateampublicmodel"></a>

```json
{
  "averageDonationAmount": 0,
  "campaign": {
    "allowsFundraisers": true,
    "allowsFundraiserSelfSignUp": true,
    "allowsTeams": true,
    "allowsTeamSelfSignUp": true,
    "donationCount": 0,
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "createdAtLocal": "2018-08-20T06:00:18Z",
  "createdAt": "2018-08-20T06:00:18Z",
  "donationCount": 0,
  "id": 0,
  "isPublic": true,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "organization": {
    "country": "string",
    "currency": "string",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "raisedAmount": 0,
  "status": "live",
  "fundraisersCount": 0,
  "targetAmount": 0,
  "template": {
    "value": {
      "property1": {},
      "property2": {}
    }
  },
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|averageDonationAmount|number(double)|false|none|none|
|campaign|[TeamCampaignPublicModel](#schemateamcampaignpublicmodel)|false|none|none|
|createdAtLocal|string(date-time)|false|read-only|none|
|createdAt|string(date-time)|false|none|none|
|donationCount|integer(int32)|false|none|none|
|id|integer(int32)|false|none|none|
|isPublic|boolean|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|organization|[TeamOrganizationPublicModel](#schemateamorganizationpublicmodel)|false|none|none|
|raisedAmount|number(double)|false|none|none|
|status|string|false|none|none|
|fundraisersCount|integer(int32)|false|none|none|
|targetAmount|number(double)|false|none|none|
|template|[DataTemplatePublicModel](#schemadatatemplatepublicmodel)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSteamcampaignpublicmodel">TeamCampaignPublicModel</h2>

<a id="schemateamcampaignpublicmodel"></a>

```json
{
  "allowsFundraisers": true,
  "allowsFundraiserSelfSignUp": true,
  "allowsTeams": true,
  "allowsTeamSelfSignUp": true,
  "donationCount": 0,
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "raisedAmount": 0,
  "status": "live",
  "targetAmount": 0,
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|allowsFundraisers|boolean|false|none|none|
|allowsFundraiserSelfSignUp|boolean|false|none|none|
|allowsTeams|boolean|false|none|none|
|allowsTeamSelfSignUp|boolean|false|none|none|
|donationCount|integer(int32)|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|raisedAmount|number(double)|false|none|none|
|status|string|false|none|none|
|targetAmount|number(double)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSteamorganizationpublicmodel">TeamOrganizationPublicModel</h2>

<a id="schemateamorganizationpublicmodel"></a>

```json
{
  "country": "string",
  "currency": "string",
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|country|string|false|none|none|
|currency|string|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

<h2 id="tocSpagesearchmodel">PageSearchModel</h2>

<a id="schemapagesearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSpageelementmodel">PageElementModel</h2>

<a id="schemapageelementmodel"></a>

```json
{
  "accountId": 0,
  "account": {
    "id": 0,
    "email": "string",
    "firstName": "string",
    "lastName": "string"
  },
  "additionalDonationsNeededForTarget": 0,
  "averageDonationAmount": 0,
  "campaignId": 0,
  "campaign": {
    "name": "string",
    "status": "live",
    "template": {
      "key": "string",
      "value": {}
    },
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "urlPath": "string"
  },
  "createdAtLocal": "2018-08-20T06:00:18Z",
  "createdAt": "2018-08-20T06:00:18Z",
  "donationCount": 0,
  "eventId": 0,
  "event": {
    "status": "live",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "urlPath": "string"
  },
  "fundraiserId": 0,
  "fundraiser": {
    "status": "live",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "urlPath": "string"
  },
  "isFundraiserOrTeam": true,
  "isActive": true,
  "isPublic": true,
  "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
  "lastUpdatedAt": "2018-08-20T06:00:18Z",
  "name": "string",
  "newsletterOptIn": true,
  "organizationId": 0,
  "organization": {
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "urlPath": "string"
  },
  "phoneNumber": "string",
  "raisedAmount": 0,
  "status": "string",
  "targetAmount": 0,
  "teamId": 0,
  "team": {
    "status": "live",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "urlPath": "string"
  },
  "type": "campaign",
  "urlPath": "string",
  "url": "string",
  "urlFull": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|accountId|integer(int32)|false|none|none|
|account|[PageAccountBasicModel](#schemapageaccountbasicmodel)|false|none|none|
|additionalDonationsNeededForTarget|number(double)|false|none|none|
|averageDonationAmount|number(double)|false|none|none|
|campaignId|integer(int32)|false|none|none|
|campaign|[PageCampaignElementModel](#schemapagecampaignelementmodel)|false|none|none|
|createdAtLocal|string(date-time)|false|read-only|none|
|createdAt|string(date-time)|false|none|none|
|donationCount|integer(int32)|false|none|none|
|eventId|integer(int32)|false|none|none|
|event|[PageEventBasicModel](#schemapageeventbasicmodel)|false|none|none|
|fundraiserId|integer(int32)|false|none|none|
|fundraiser|[PageFundraiserBasicModel](#schemapagefundraiserbasicmodel)|false|none|none|
|isFundraiserOrTeam|boolean|false|none|none|
|isActive|boolean|false|none|none|
|isPublic|boolean|false|none|none|
|lastUpdatedAtLocal|string(date-time)|false|read-only|none|
|lastUpdatedAt|string(date-time)|false|none|none|
|name|string|false|none|none|
|newsletterOptIn|boolean|false|none|none|
|organizationId|integer(int32)|false|none|none|
|organization|[PageOrganizationBasicModel](#schemapageorganizationbasicmodel)|false|none|none|
|phoneNumber|string|false|none|none|
|raisedAmount|number(double)|false|none|none|
|status|string|false|read-only|none|
|targetAmount|number(double)|false|none|none|
|teamId|integer(int32)|false|none|none|
|team|[PageTeamBasicModel](#schemapageteambasicmodel)|false|none|none|
|type|string|false|none|none|
|urlPath|string|false|none|none|
|url|string|false|read-only|none|
|urlFull|string|false|read-only|none|

#### Enumerated Values

|Property|Value|
|---|---|
|type|campaign|
|type|fundraiser|
|type|team|

<h2 id="tocSpageaccountbasicmodel">PageAccountBasicModel</h2>

<a id="schemapageaccountbasicmodel"></a>

```json
{
  "id": 0,
  "email": "string",
  "firstName": "string",
  "lastName": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|email|string|false|none|none|
|firstName|string|false|none|none|
|lastName|string|false|none|none|

<h2 id="tocSpagecampaignelementmodel">PageCampaignElementModel</h2>

<a id="schemapagecampaignelementmodel"></a>

```json
{
  "name": "string",
  "status": "live",
  "template": {
    "key": "string",
    "value": {}
  },
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|false|none|none|
|status|string|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSpageeventbasicmodel">PageEventBasicModel</h2>

<a id="schemapageeventbasicmodel"></a>

```json
{
  "status": "live",
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|status|string|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSpagefundraiserbasicmodel">PageFundraiserBasicModel</h2>

<a id="schemapagefundraiserbasicmodel"></a>

```json
{
  "status": "live",
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|status|string|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSpageorganizationbasicmodel">PageOrganizationBasicModel</h2>

<a id="schemapageorganizationbasicmodel"></a>

```json
{
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|urlPath|string|false|none|none|

<h2 id="tocSpageteambasicmodel">PageTeamBasicModel</h2>

<a id="schemapageteambasicmodel"></a>

```json
{
  "status": "live",
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|status|string|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSpagepublicsearchmodel">PagePublicSearchModel</h2>

<a id="schemapagepublicsearchmodel"></a>

```json
{
  "primaryUrlPath": "string",
  "secondaryUrlPath": "string",
  "tertiaryUrlPath": "string",
  "type": "campaign",
  "isFundraiserOrTeam": true,
  "inactiveOnly": true,
  "text": "string",
  "page": 0,
  "orderKey": "string",
  "orderDirection": "asc"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|primaryUrlPath|string|false|none|none|
|secondaryUrlPath|string|false|none|none|
|tertiaryUrlPath|string|false|none|none|
|type|string|false|none|none|
|isFundraiserOrTeam|boolean|false|none|none|
|inactiveOnly|boolean|false|none|none|
|text|string|false|none|none|
|page|integer(int32)|false|none|none|
|orderKey|string|false|none|none|
|orderDirection|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|type|campaign|
|type|fundraiser|
|type|team|
|orderDirection|asc|
|orderDirection|desc|

<h2 id="tocSpagepublicmodel">PagePublicModel</h2>

<a id="schemapagepublicmodel"></a>

```json
{
  "additionalDonationsNeededForTarget": 0,
  "averageDonationAmount": 0,
  "createdAtLocal": "2018-08-20T06:00:18Z",
  "createdAt": "2018-08-20T06:00:18Z",
  "campaignId": 0,
  "campaign": {
    "name": "string",
    "status": "live",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "urlPath": "string"
  },
  "donationCount": 0,
  "event": {
    "status": "live",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "urlPath": "string"
  },
  "fundraiserId": 0,
  "fundraiser": {
    "status": "live",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "urlPath": "string"
  },
  "name": "string",
  "organizationId": 0,
  "organization": {
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "urlPath": "string"
  },
  "raisedAmount": 0,
  "status": "string",
  "targetAmount": 0,
  "teamId": 0,
  "team": {
    "status": "live",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "urlPath": "string"
  },
  "type": "campaign",
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|additionalDonationsNeededForTarget|number(double)|false|none|none|
|averageDonationAmount|number(double)|false|none|none|
|createdAtLocal|string(date-time)|false|read-only|none|
|createdAt|string(date-time)|false|none|none|
|campaignId|integer(int32)|false|none|none|
|campaign|[PageCampaignBasicModel](#schemapagecampaignbasicmodel)|false|none|none|
|donationCount|integer(int32)|false|none|none|
|event|[PageEventBasicModel](#schemapageeventbasicmodel)|false|none|none|
|fundraiserId|integer(int32)|false|none|none|
|fundraiser|[PageFundraiserBasicModel](#schemapagefundraiserbasicmodel)|false|none|none|
|name|string|false|none|none|
|organizationId|integer(int32)|false|none|none|
|organization|[PageOrganizationBasicModel](#schemapageorganizationbasicmodel)|false|none|none|
|raisedAmount|number(double)|false|none|none|
|status|string|false|read-only|none|
|targetAmount|number(double)|false|none|none|
|teamId|integer(int32)|false|none|none|
|team|[PageTeamBasicModel](#schemapageteambasicmodel)|false|none|none|
|type|string|false|none|none|
|url|string|false|read-only|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|type|campaign|
|type|fundraiser|
|type|team|

<h2 id="tocSpagecampaignbasicmodel">PageCampaignBasicModel</h2>

<a id="schemapagecampaignbasicmodel"></a>

```json
{
  "name": "string",
  "status": "live",
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|false|none|none|
|status|string|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSsessionelementmodel">SessionElementModel</h2>

<a id="schemasessionelementmodel"></a>

```json
{
  "key": "string",
  "account": {
    "id": 0,
    "firstName": "string",
    "lastName": "string",
    "source": "default"
  },
  "organization": {
    "id": 0,
    "name": "string"
  },
  "expiry": "2018-08-20T06:00:18Z",
  "impersonated": true,
  "impersonator": {
    "id": 0,
    "firstName": "string",
    "lastName": "string",
    "source": "default"
  },
  "isFundraiser": true,
  "isSystemAdmin": true,
  "isOrganizationAdmin": true,
  "refresh": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|key|string|false|none|none|
|account|[SessionAccountModel](#schemasessionaccountmodel)|false|none|none|
|organization|[SessionOrganizationModel](#schemasessionorganizationmodel)|false|none|none|
|expiry|string(date-time)|false|none|none|
|impersonated|boolean|false|read-only|none|
|impersonator|[SessionAccountModel](#schemasessionaccountmodel)|false|none|none|
|isFundraiser|boolean|false|none|none|
|isSystemAdmin|boolean|false|none|none|
|isOrganizationAdmin|boolean|false|none|none|
|refresh|string|false|none|none|

<h2 id="tocSsessionaccountmodel">SessionAccountModel</h2>

<a id="schemasessionaccountmodel"></a>

```json
{
  "id": 0,
  "firstName": "string",
  "lastName": "string",
  "source": "default"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|firstName|string|false|none|none|
|lastName|string|false|none|none|
|source|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|source|default|
|source|facebook|
|source|google|

<h2 id="tocSsessionorganizationmodel">SessionOrganizationModel</h2>

<a id="schemasessionorganizationmodel"></a>

```json
{
  "id": 0,
  "name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|

<h2 id="tocSsessioncreatemodel">SessionCreateModel</h2>

<a id="schemasessioncreatemodel"></a>

```json
{
  "email": "string",
  "password": "string",
  "remember": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|false|none|none|
|password|string|false|none|none|
|remember|boolean|false|none|none|

<h2 id="tocSsessionfacebookloginmodel">SessionFacebookLoginModel</h2>

<a id="schemasessionfacebookloginmodel"></a>

```json
{
  "accessCode": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|accessCode|string|false|none|none|

<h2 id="tocSsessionpasswordlesseditmodel">SessionPasswordLessEditModel</h2>

<a id="schemasessionpasswordlesseditmodel"></a>

```json
{
  "email": "string",
  "returnUrl": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|false|none|none|
|returnUrl|string|false|none|none|

<h2 id="tocSsessionactivateeditmodel">SessionActivateEditModel</h2>

<a id="schemasessionactivateeditmodel"></a>

```json
{
  "id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|false|none|none|

<h2 id="tocSsessionrefresheditmodel">SessionRefreshEditModel</h2>

<a id="schemasessionrefresheditmodel"></a>

```json
{
  "accountId": 0,
  "code": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|accountId|integer(int32)|false|none|none|
|code|string|false|none|none|

<h2 id="tocSsessionimpersonatemodel">SessionImpersonateModel</h2>

<a id="schemasessionimpersonatemodel"></a>

```json
{
  "accountId": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|accountId|integer(int32)|false|none|none|

<h2 id="tocSteamelementmodel">TeamElementModel</h2>

<a id="schemateamelementmodel"></a>

```json
{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "averageDonationAmount": 0,
  "campaignId": 0,
  "campaign": {
    "allowsFundraisers": true,
    "allowsFundraiserSelfSignUp": true,
    "allowsTeams": true,
    "allowsTeamSelfSignUp": true,
    "donationCount": 0,
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "createdAtLocal": "2018-08-20T06:00:18Z",
  "createdAt": "2018-08-20T06:00:18Z",
  "donationCount": 0,
  "id": 0,
  "isPublic": true,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "manager": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "id": 0
  },
  "name": "string",
  "newsletter": true,
  "organization": {
    "country": "string",
    "currency": "string",
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "phoneNumber": "string",
  "raisedAmount": 0,
  "status": "live",
  "fundraisersActiveCount": 0,
  "fundraisersCount": 0,
  "targetAmount": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|address|[TeamAddressModel](#schemateamaddressmodel)|false|none|none|
|averageDonationAmount|number(double)|false|none|none|
|campaignId|integer(int32)|false|none|none|
|campaign|[TeamCampaignModel](#schemateamcampaignmodel)|false|none|none|
|createdAtLocal|string(date-time)|false|read-only|none|
|createdAt|string(date-time)|false|none|none|
|donationCount|integer(int32)|false|none|none|
|id|integer(int32)|false|none|none|
|isPublic|boolean|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|manager|[TeamManagerModel](#schemateammanagermodel)|false|none|none|
|name|string|false|none|none|
|newsletter|boolean|false|none|none|
|organization|[TeamOrganizationModel](#schemateamorganizationmodel)|false|none|none|
|phoneNumber|string|false|none|none|
|raisedAmount|number(double)|false|none|none|
|status|string|false|none|none|
|fundraisersActiveCount|integer(int32)|false|none|none|
|fundraisersCount|integer(int32)|false|none|none|
|targetAmount|number(double)|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSteamaddressmodel">TeamAddressModel</h2>

<a id="schemateamaddressmodel"></a>

```json
{
  "street": "string",
  "city": "string",
  "state": "string",
  "postcode": "string",
  "country": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|street|string|false|none|none|
|city|string|false|none|none|
|state|string|false|none|none|
|postcode|string|false|none|none|
|country|string|false|none|none|

<h2 id="tocSteamcampaignmodel">TeamCampaignModel</h2>

<a id="schemateamcampaignmodel"></a>

```json
{
  "allowsFundraisers": true,
  "allowsFundraiserSelfSignUp": true,
  "allowsTeams": true,
  "allowsTeamSelfSignUp": true,
  "donationCount": 0,
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "raisedAmount": 0,
  "status": "live",
  "targetAmount": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|allowsFundraisers|boolean|false|none|none|
|allowsFundraiserSelfSignUp|boolean|false|none|none|
|allowsTeams|boolean|false|none|none|
|allowsTeamSelfSignUp|boolean|false|none|none|
|donationCount|integer(int32)|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|raisedAmount|number(double)|false|none|none|
|status|string|false|none|none|
|targetAmount|number(double)|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSteammanagermodel">TeamManagerModel</h2>

<a id="schemateammanagermodel"></a>

```json
{
  "email": "string",
  "firstName": "string",
  "lastName": "string",
  "id": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|false|none|none|
|firstName|string|false|none|none|
|lastName|string|false|none|none|
|id|integer(int32)|false|none|none|

<h2 id="tocSteamorganizationmodel">TeamOrganizationModel</h2>

<a id="schemateamorganizationmodel"></a>

```json
{
  "country": "string",
  "currency": "string",
  "id": 0,
  "mainImagePath": "string",
  "mainImageUrl": "string",
  "name": "string",
  "template": {
    "key": "string",
    "value": {}
  },
  "url": "string",
  "urlFull": "string",
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|country|string|false|none|none|
|currency|string|false|none|none|
|id|integer(int32)|false|none|none|
|mainImagePath|string|false|none|none|
|mainImageUrl|string|false|none|none|
|name|string|false|none|none|
|template|[DataTemplateElementModel](#schemadatatemplateelementmodel)|false|none|none|
|url|string|false|none|none|
|urlFull|string|false|read-only|none|
|urlPath|string|false|none|none|

<h2 id="tocSteameditmodel">TeamEditModel</h2>

<a id="schemateameditmodel"></a>

```json
{
  "address": {
    "street": "string",
    "city": "string",
    "state": "string",
    "postcode": "string",
    "country": "string"
  },
  "campaignId": 0,
  "customFields": [
    {
      "identifier": "string",
      "value": {}
    }
  ],
  "isPublic": true,
  "mainImagePath": "string",
  "manager": {
    "operation": "unchanged",
    "email": "string",
    "customInviteUrl": "string"
  },
  "name": "string",
  "newsletter": true,
  "phoneNumber": "string",
  "removeAllFundraisers": true,
  "status": "live",
  "targetAmount": 0,
  "template": {
    "key": "string",
    "value": {}
  },
  "urlPath": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|address|[TeamAddressEditModel](#schemateamaddresseditmodel)|false|none|none|
|campaignId|integer(int32)|false|none|none|
|customFields|[[CustomFieldValueEditModel](#schemacustomfieldvalueeditmodel)]|false|none|none|
|isPublic|boolean|false|none|none|
|mainImagePath|string|false|none|none|
|manager|[TeamManagerEditModel](#schemateammanagereditmodel)|false|none|none|
|name|string|false|none|none|
|newsletter|boolean|false|none|none|
|phoneNumber|string|false|none|none|
|removeAllFundraisers|boolean|false|none|none|
|status|string|false|none|none|
|targetAmount|number(double)|false|none|none|
|template|[DataTemplateEditModel](#schemadatatemplateeditmodel)|false|none|none|
|urlPath|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|status|live|
|status|completed|
|status|archived|

<h2 id="tocSteamaddresseditmodel">TeamAddressEditModel</h2>

<a id="schemateamaddresseditmodel"></a>

```json
{
  "street": "string",
  "city": "string",
  "state": "string",
  "postcode": "string",
  "country": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|street|string|false|none|none|
|city|string|false|none|none|
|state|string|false|none|none|
|postcode|string|false|none|none|
|country|string|false|none|none|

<h2 id="tocSteammanagereditmodel">TeamManagerEditModel</h2>

<a id="schemateammanagereditmodel"></a>

```json
{
  "operation": "unchanged",
  "email": "string",
  "customInviteUrl": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|operation|string|false|none|none|
|email|string|false|none|none|
|customInviteUrl|string|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|operation|unchanged|
|operation|remove|
|operation|new|
|operation|fromCredential|

<h2 id="tocSteamsearchmodel">TeamSearchModel</h2>

<a id="schemateamsearchmodel"></a>

```json
{
  "filters": [
    {
      "key": "string",
      "operator": "equalTo",
      "value": "string"
    }
  ],
  "text": "string",
  "orderBy": {
    "key": "string",
    "direction": "asc"
  },
  "page": 0,
  "pageSize": 0,
  "resultType": "lookup",
  "includeDataTemplate": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|filters|[[ListFilter](#schemalistfilter)]|false|none|none|
|text|string|false|none|none|
|orderBy|[ListOrderBy](#schemalistorderby)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|resultType|string|false|none|none|
|includeDataTemplate|boolean|false|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|resultType|lookup|
|resultType|basic|
|resultType|full|

<h2 id="tocSscalaractionresult_accesskeyelementmodel_">ScalarActionResult_AccessKeyElementModel_</h2>

<a id="schemascalaractionresult_accesskeyelementmodel_"></a>

```json
{
  "data": {
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "clientKey": "string",
    "description": "string",
    "createdAt": "2018-08-20T06:00:18Z"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[AccessKeyElementModel](#schemaaccesskeyelementmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSscalaractionresult_donationelementmodel_">ScalarActionResult_DonationElementModel_</h2>

<a id="schemascalaractionresult_donationelementmodel_"></a>

```json
{
  "data": {
    "accountId": 0,
    "amount": 0,
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string",
      "template": {
        "key": "string",
        "value": {}
      }
    },
    "donatedAtLocal": "2018-08-20T06:00:18Z",
    "donatedAt": "2018-08-20T06:00:18Z",
    "donor": {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "anonymous": true,
      "businessName": "string",
      "donorId": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "newsletter": true,
      "phoneNumber": "string"
    },
    "financials": {
      "cardBrand": "string",
      "cardCountry": "string",
      "cardLast4Digits": "string",
      "currency": "string",
      "fee": 0,
      "feeCovered": true,
      "platform": "stripe",
      "refunded": true,
      "refundedAt": "2018-08-20T06:00:18Z",
      "refundedAtLocal": "2018-08-20T06:00:18Z",
      "subscription": true,
      "tax": 0,
      "totalFees": 0,
      "timezone": "string"
    },
    "fundraiserId": 0,
    "fundraiser": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAt": "2018-08-20T06:00:18Z",
    "message": "string",
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    },
    "pageType": "campaign",
    "receiptNumber": "string",
    "reply": {
      "displayFirstName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "repliedAtLocal": "2018-08-20T06:00:18Z",
      "repliedAt": "2018-08-20T06:00:18Z",
      "reply": "string"
    },
    "status": "collectedFromCustomer",
    "teamId": 0,
    "team": {
      "id": 0,
      "name": "string",
      "urlPath": "string",
      "url": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "type": "online"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[DonationElementModel](#schemadonationelementmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSlistactionresult_accesskeyelementmodel_">ListActionResult_AccessKeyElementModel_</h2>

<a id="schemalistactionresult_accesskeyelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "organizationId": 0,
        "organization": {
          "id": 0,
          "name": "string",
          "urlPath": "string"
        },
        "clientKey": "string",
        "description": "string",
        "createdAt": "2018-08-20T06:00:18Z"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_AccessKeyElementModel_](#schemapagedlist_accesskeyelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_accesskeyelementmodel_">PagedList_AccessKeyElementModel_</h2>

<a id="schemapagedlist_accesskeyelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "organizationId": 0,
      "organization": {
        "id": 0,
        "name": "string",
        "urlPath": "string"
      },
      "clientKey": "string",
      "description": "string",
      "createdAt": "2018-08-20T06:00:18Z"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[AccessKeyElementModel](#schemaaccesskeyelementmodel)]|false|none|none|

<h2 id="tocSscalaractionresult_metadatapublicmodel_">ScalarActionResult_MetadataPublicModel_</h2>

<a id="schemascalaractionresult_metadatapublicmodel_"></a>

```json
{
  "data": {
    "columns": [
      {
        "key": "string",
        "dataType": "string",
        "additionalData": {}
      }
    ],
    "filters": [
      "string"
    ],
    "sort": [
      "string"
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[MetadataPublicModel](#schemametadatapublicmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSscalaractionresult_accountelementmodel_">ScalarActionResult_AccountElementModel_</h2>

<a id="schemascalaractionresult_accountelementmodel_"></a>

```json
{
  "data": {
    "id": 0,
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "createdAt": "2018-08-20T06:00:18Z",
    "lastLoggedInAt": "2018-08-20T06:00:18Z",
    "status": "active",
    "roles": "notDefined",
    "isOrgAdmin": true,
    "isSysAdmin": true,
    "isFundraiser": true,
    "isAdmin": true,
    "organizationId": 0,
    "source": "default",
    "organization": {
      "id": 0,
      "name": "string",
      "urlPath": "string"
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[AccountElementModel](#schemaaccountelementmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSscalaractionresult_accountpublicmodel_">ScalarActionResult_AccountPublicModel_</h2>

<a id="schemascalaractionresult_accountpublicmodel_"></a>

```json
{
  "data": {
    "email": "string",
    "firstName": "string",
    "lastName": "string",
    "sessionKey": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[AccountPublicModel](#schemaaccountpublicmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSscalaractionresult_string_">ScalarActionResult_String_</h2>

<a id="schemascalaractionresult_string_"></a>

```json
{
  "data": "string",
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|string|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSlistactionresult_accountelementmodel_">ListActionResult_AccountElementModel_</h2>

<a id="schemalistactionresult_accountelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "id": 0,
        "email": "string",
        "firstName": "string",
        "lastName": "string",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "createdAt": "2018-08-20T06:00:18Z",
        "lastLoggedInAt": "2018-08-20T06:00:18Z",
        "status": "active",
        "roles": "notDefined",
        "isOrgAdmin": true,
        "isSysAdmin": true,
        "isFundraiser": true,
        "isAdmin": true,
        "organizationId": 0,
        "source": "default",
        "organization": {
          "id": 0,
          "name": "string",
          "urlPath": "string"
        }
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_AccountElementModel_](#schemapagedlist_accountelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_accountelementmodel_">PagedList_AccountElementModel_</h2>

<a id="schemapagedlist_accountelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "id": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "createdAt": "2018-08-20T06:00:18Z",
      "lastLoggedInAt": "2018-08-20T06:00:18Z",
      "status": "active",
      "roles": "notDefined",
      "isOrgAdmin": true,
      "isSysAdmin": true,
      "isFundraiser": true,
      "isAdmin": true,
      "organizationId": 0,
      "source": "default",
      "organization": {
        "id": 0,
        "name": "string",
        "urlPath": "string"
      }
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[AccountElementModel](#schemaaccountelementmodel)]|false|none|none|

<h2 id="tocSscalaractionresult_decimal_">ScalarActionResult_Decimal_</h2>

<a id="schemascalaractionresult_decimal_"></a>

```json
{
  "data": 0,
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|number(double)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSlistactionresult_accountdonorelementmodel_">ListActionResult_AccountDonorElementModel_</h2>

<a id="schemalistactionresult_accountdonorelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "id": 0,
        "email": "string",
        "firstName": "string",
        "lastName": "string",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "createdAt": "2018-08-20T06:00:18Z",
        "donationCount": 0,
        "raisedAmount": 0,
        "averageDonationAmount": 0
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_AccountDonorElementModel_](#schemapagedlist_accountdonorelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_accountdonorelementmodel_">PagedList_AccountDonorElementModel_</h2>

<a id="schemapagedlist_accountdonorelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "id": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "raisedAmount": 0,
      "averageDonationAmount": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[AccountDonorElementModel](#schemaaccountdonorelementmodel)]|false|none|none|

<h2 id="tocSlistactionresult_accountfundraiserelementmodel_">ListActionResult_AccountFundraiserElementModel_</h2>

<a id="schemalistactionresult_accountfundraiserelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "id": 0,
        "email": "string",
        "firstName": "string",
        "lastName": "string",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "createdAt": "2018-08-20T06:00:18Z",
        "donationCount": 0,
        "raisedAmount": 0,
        "averageDonationAmount": 0,
        "activePagesCount": 0,
        "pagesCount": 0
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_AccountFundraiserElementModel_](#schemapagedlist_accountfundraiserelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_accountfundraiserelementmodel_">PagedList_AccountFundraiserElementModel_</h2>

<a id="schemapagedlist_accountfundraiserelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "id": 0,
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "raisedAmount": 0,
      "averageDonationAmount": 0,
      "activePagesCount": 0,
      "pagesCount": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[AccountFundraiserElementModel](#schemaaccountfundraiserelementmodel)]|false|none|none|

<h2 id="tocSscalaractionresult_campaignelementmodel_">ScalarActionResult_CampaignElementModel_</h2>

<a id="schemascalaractionresult_campaignelementmodel_"></a>

```json
{
  "data": {
    "activePagesCount": 0,
    "additionalDonationsNeededForTarget": 0,
    "averageDonationAmount": 0,
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "dataCapture": {
      "registration": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      },
      "donation": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      }
    },
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "fundraisersActiveCount": 0,
    "fundraisersCount": 0,
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "id": 0,
    "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
    "lastUpdatedAtUtc": "2018-08-20T06:00:18Z",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organizationId": 0,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "organizationPaymentPlatformId": 0,
    "pagesCount": 0,
    "paymentPlatforms": {
      "main": {
        "id": 0,
        "platform": "stripe",
        "platformType": "creditCardForm",
        "publicKey": "string"
      },
      "alternative": [
        {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        }
      ]
    },
    "raisedAmount": 0,
    "targetAmount": 0,
    "type": "default",
    "status": "live",
    "teamsActiveCount": 0,
    "teamsCount": 0,
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[CampaignElementModel](#schemacampaignelementmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocScampaignpaymentplatforms_campaignpaymentplatformelementmodel_">CampaignPaymentPlatforms_CampaignPaymentPlatformElementModel_</h2>

<a id="schemacampaignpaymentplatforms_campaignpaymentplatformelementmodel_"></a>

```json
{
  "main": {
    "id": 0,
    "platform": "stripe",
    "platformType": "creditCardForm",
    "publicKey": "string"
  },
  "alternative": [
    {
      "id": 0,
      "platform": "stripe",
      "platformType": "creditCardForm",
      "publicKey": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|main|[CampaignPaymentPlatformElementModel](#schemacampaignpaymentplatformelementmodel)|false|none|none|
|alternative|[[CampaignPaymentPlatformElementModel](#schemacampaignpaymentplatformelementmodel)]|false|none|none|

<h2 id="tocSscalaractionresult_campaignpublicmodel_">ScalarActionResult_CampaignPublicModel_</h2>

<a id="schemascalaractionresult_campaignpublicmodel_"></a>

```json
{
  "data": {
    "additionalDonationsNeededForTarget": 0,
    "averageDonationAmount": 0,
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "dataCapture": {
      "registration": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      },
      "donation": {
        "phone": {
          "capture": true,
          "mandatory": true
        },
        "address": {
          "capture": true,
          "mandatory": true
        }
      }
    },
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "fundraisersCount": 0,
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "id": 0,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organizationId": 0,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "pagesCount": 0,
    "paymentPlatforms": {
      "main": {
        "id": 0,
        "platform": "stripe",
        "platformType": "creditCardForm",
        "publicKey": "string"
      },
      "alternative": [
        {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        }
      ]
    },
    "raisedAmount": 0,
    "targetAmount": 0,
    "type": "default",
    "status": "live",
    "teamsCount": 0,
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[CampaignPublicModel](#schemacampaignpublicmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSlistactionresult_campaignelementmodel_">ListActionResult_CampaignElementModel_</h2>

<a id="schemalistactionresult_campaignelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "activePagesCount": 0,
        "additionalDonationsNeededForTarget": 0,
        "averageDonationAmount": 0,
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "dataCapture": {
          "registration": {
            "phone": {
              "capture": true,
              "mandatory": true
            },
            "address": {
              "capture": true,
              "mandatory": true
            }
          },
          "donation": {
            "phone": {
              "capture": true,
              "mandatory": true
            },
            "address": {
              "capture": true,
              "mandatory": true
            }
          }
        },
        "donationCount": 0,
        "donationSetup": {
          "allowRecurringGiving": true
        },
        "fundraisersActiveCount": 0,
        "fundraisersCount": 0,
        "fundraisers": {
          "enabled": true,
          "defaultTargetAmount": 0,
          "allowSelfSignUp": true
        },
        "id": 0,
        "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
        "lastUpdatedAtUtc": "2018-08-20T06:00:18Z",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "organizationId": 0,
        "organization": {
          "country": "string",
          "currency": "string",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "organizationPaymentPlatformId": 0,
        "pagesCount": 0,
        "paymentPlatforms": {
          "main": {
            "id": 0,
            "platform": "stripe",
            "platformType": "creditCardForm",
            "publicKey": "string"
          },
          "alternative": [
            {
              "id": 0,
              "platform": "stripe",
              "platformType": "creditCardForm",
              "publicKey": "string"
            }
          ]
        },
        "raisedAmount": 0,
        "targetAmount": 0,
        "type": "default",
        "status": "live",
        "teamsActiveCount": 0,
        "teamsCount": 0,
        "teams": {
          "enabled": true,
          "defaultTargetAmount": 0,
          "allowSelfSignUp": true
        },
        "template": {
          "key": "string",
          "value": {}
        },
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_CampaignElementModel_](#schemapagedlist_campaignelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_campaignelementmodel_">PagedList_CampaignElementModel_</h2>

<a id="schemapagedlist_campaignelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "activePagesCount": 0,
      "additionalDonationsNeededForTarget": 0,
      "averageDonationAmount": 0,
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "dataCapture": {
        "registration": {
          "phone": {
            "capture": true,
            "mandatory": true
          },
          "address": {
            "capture": true,
            "mandatory": true
          }
        },
        "donation": {
          "phone": {
            "capture": true,
            "mandatory": true
          },
          "address": {
            "capture": true,
            "mandatory": true
          }
        }
      },
      "donationCount": 0,
      "donationSetup": {
        "allowRecurringGiving": true
      },
      "fundraisersActiveCount": 0,
      "fundraisersCount": 0,
      "fundraisers": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "id": 0,
      "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
      "lastUpdatedAtUtc": "2018-08-20T06:00:18Z",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organizationId": 0,
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "template": {
          "key": "string",
          "value": {}
        },
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "organizationPaymentPlatformId": 0,
      "pagesCount": 0,
      "paymentPlatforms": {
        "main": {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        },
        "alternative": [
          {
            "id": 0,
            "platform": "stripe",
            "platformType": "creditCardForm",
            "publicKey": "string"
          }
        ]
      },
      "raisedAmount": 0,
      "targetAmount": 0,
      "type": "default",
      "status": "live",
      "teamsActiveCount": 0,
      "teamsCount": 0,
      "teams": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[CampaignElementModel](#schemacampaignelementmodel)]|false|none|none|

<h2 id="tocSscalaractionresult_donationfeecalculationelementmodel_">ScalarActionResult_DonationFeeCalculationElementModel_</h2>

<a id="schemascalaractionresult_donationfeecalculationelementmodel_"></a>

```json
{
  "data": {
    "amount": 0,
    "fee": 0,
    "tax": 0,
    "totalFees": 0,
    "totalWithFees": 0
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[DonationFeeCalculationElementModel](#schemadonationfeecalculationelementmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSlistactionresult_donationelementmodel_">ListActionResult_DonationElementModel_</h2>

<a id="schemalistactionresult_donationelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "accountId": 0,
        "amount": 0,
        "campaignId": 0,
        "campaign": {
          "id": 0,
          "name": "string",
          "urlPath": "string",
          "url": "string",
          "template": {
            "key": "string",
            "value": {}
          }
        },
        "donatedAtLocal": "2018-08-20T06:00:18Z",
        "donatedAt": "2018-08-20T06:00:18Z",
        "donor": {
          "address": {
            "street": "string",
            "city": "string",
            "state": "string",
            "postcode": "string",
            "country": "string"
          },
          "anonymous": true,
          "businessName": "string",
          "donorId": 0,
          "email": "string",
          "firstName": "string",
          "lastName": "string",
          "newsletter": true,
          "phoneNumber": "string"
        },
        "financials": {
          "cardBrand": "string",
          "cardCountry": "string",
          "cardLast4Digits": "string",
          "currency": "string",
          "fee": 0,
          "feeCovered": true,
          "platform": "stripe",
          "refunded": true,
          "refundedAt": "2018-08-20T06:00:18Z",
          "refundedAtLocal": "2018-08-20T06:00:18Z",
          "subscription": true,
          "tax": 0,
          "totalFees": 0,
          "timezone": "string"
        },
        "fundraiserId": 0,
        "fundraiser": {
          "id": 0,
          "name": "string",
          "urlPath": "string",
          "url": "string"
        },
        "id": 0,
        "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
        "lastUpdatedAt": "2018-08-20T06:00:18Z",
        "message": "string",
        "organizationId": 0,
        "organization": {
          "id": 0,
          "name": "string",
          "urlPath": "string"
        },
        "pageType": "campaign",
        "receiptNumber": "string",
        "reply": {
          "displayFirstName": "string",
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "repliedAtLocal": "2018-08-20T06:00:18Z",
          "repliedAt": "2018-08-20T06:00:18Z",
          "reply": "string"
        },
        "status": "collectedFromCustomer",
        "teamId": 0,
        "team": {
          "id": 0,
          "name": "string",
          "urlPath": "string",
          "url": "string"
        },
        "template": {
          "key": "string",
          "value": {}
        },
        "timezone": "string",
        "type": "online"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_DonationElementModel_](#schemapagedlist_donationelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_donationelementmodel_">PagedList_DonationElementModel_</h2>

<a id="schemapagedlist_donationelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "accountId": 0,
      "amount": 0,
      "campaignId": 0,
      "campaign": {
        "id": 0,
        "name": "string",
        "urlPath": "string",
        "url": "string",
        "template": {
          "key": "string",
          "value": {}
        }
      },
      "donatedAtLocal": "2018-08-20T06:00:18Z",
      "donatedAt": "2018-08-20T06:00:18Z",
      "donor": {
        "address": {
          "street": "string",
          "city": "string",
          "state": "string",
          "postcode": "string",
          "country": "string"
        },
        "anonymous": true,
        "businessName": "string",
        "donorId": 0,
        "email": "string",
        "firstName": "string",
        "lastName": "string",
        "newsletter": true,
        "phoneNumber": "string"
      },
      "financials": {
        "cardBrand": "string",
        "cardCountry": "string",
        "cardLast4Digits": "string",
        "currency": "string",
        "fee": 0,
        "feeCovered": true,
        "platform": "stripe",
        "refunded": true,
        "refundedAt": "2018-08-20T06:00:18Z",
        "refundedAtLocal": "2018-08-20T06:00:18Z",
        "subscription": true,
        "tax": 0,
        "totalFees": 0,
        "timezone": "string"
      },
      "fundraiserId": 0,
      "fundraiser": {
        "id": 0,
        "name": "string",
        "urlPath": "string",
        "url": "string"
      },
      "id": 0,
      "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
      "lastUpdatedAt": "2018-08-20T06:00:18Z",
      "message": "string",
      "organizationId": 0,
      "organization": {
        "id": 0,
        "name": "string",
        "urlPath": "string"
      },
      "pageType": "campaign",
      "receiptNumber": "string",
      "reply": {
        "displayFirstName": "string",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "repliedAtLocal": "2018-08-20T06:00:18Z",
        "repliedAt": "2018-08-20T06:00:18Z",
        "reply": "string"
      },
      "status": "collectedFromCustomer",
      "teamId": 0,
      "team": {
        "id": 0,
        "name": "string",
        "urlPath": "string",
        "url": "string"
      },
      "template": {
        "key": "string",
        "value": {}
      },
      "timezone": "string",
      "type": "online"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[DonationElementModel](#schemadonationelementmodel)]|false|none|none|

<h2 id="tocSlistactionresult_donationpublicresultmodel_">ListActionResult_DonationPublicResultModel_</h2>

<a id="schemalistactionresult_donationpublicresultmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "amount": 0,
        "anonymous": true,
        "donatedAtLocal": "2018-08-20T06:00:18Z",
        "donatedAt": "2018-08-20T06:00:18Z",
        "donorDisplayName": "string",
        "id": 0,
        "message": "string",
        "pageType": "campaign",
        "reply": {
          "displayFirstName": "string",
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "repliedAtLocal": "2018-08-20T06:00:18Z",
          "repliedAt": "2018-08-20T06:00:18Z",
          "reply": "string"
        },
        "type": "online"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_DonationPublicResultModel_](#schemapagedlist_donationpublicresultmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_donationpublicresultmodel_">PagedList_DonationPublicResultModel_</h2>

<a id="schemapagedlist_donationpublicresultmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "amount": 0,
      "anonymous": true,
      "donatedAtLocal": "2018-08-20T06:00:18Z",
      "donatedAt": "2018-08-20T06:00:18Z",
      "donorDisplayName": "string",
      "id": 0,
      "message": "string",
      "pageType": "campaign",
      "reply": {
        "displayFirstName": "string",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "repliedAtLocal": "2018-08-20T06:00:18Z",
        "repliedAt": "2018-08-20T06:00:18Z",
        "reply": "string"
      },
      "type": "online"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[DonationPublicResultModel](#schemadonationpublicresultmodel)]|false|none|none|

<h2 id="tocSscalaractionresult_donationfeeelementmodel_">ScalarActionResult_DonationFeeElementModel_</h2>

<a id="schemascalaractionresult_donationfeeelementmodel_"></a>

```json
{
  "data": {
    "organizationId": 0,
    "organization": {
      "id": 0,
      "name": "string"
    },
    "eventId": 0,
    "event": {
      "id": 0,
      "name": "string"
    },
    "campaignId": 0,
    "campaign": {
      "id": 0,
      "name": "string"
    },
    "fee": 0,
    "feeType": "flatPercentage"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[DonationFeeElementModel](#schemadonationfeeelementmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSlistactionresult_donationfeeelementmodel_">ListActionResult_DonationFeeElementModel_</h2>

<a id="schemalistactionresult_donationfeeelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "organizationId": 0,
        "organization": {
          "id": 0,
          "name": "string"
        },
        "eventId": 0,
        "event": {
          "id": 0,
          "name": "string"
        },
        "campaignId": 0,
        "campaign": {
          "id": 0,
          "name": "string"
        },
        "fee": 0,
        "feeType": "flatPercentage"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_DonationFeeElementModel_](#schemapagedlist_donationfeeelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_donationfeeelementmodel_">PagedList_DonationFeeElementModel_</h2>

<a id="schemapagedlist_donationfeeelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "organizationId": 0,
      "organization": {
        "id": 0,
        "name": "string"
      },
      "eventId": 0,
      "event": {
        "id": 0,
        "name": "string"
      },
      "campaignId": 0,
      "campaign": {
        "id": 0,
        "name": "string"
      },
      "fee": 0,
      "feeType": "flatPercentage"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[DonationFeeElementModel](#schemadonationfeeelementmodel)]|false|none|none|

<h2 id="tocSscalaractionresult_eventelementmodel_">ScalarActionResult_EventElementModel_</h2>

<a id="schemascalaractionresult_eventelementmodel_"></a>

```json
{
  "data": {
    "id": 0,
    "organizationId": 0,
    "organizationFee": 0,
    "name": "string",
    "createdAt": "2018-08-20T06:00:18Z",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "urlPath": "string",
    "status": "live",
    "targetAmount": 0,
    "averageDonationAmount": 0,
    "raisedAmount": 0,
    "donationCount": 0,
    "donationSetup": {
      "allowRecurringGiving": true
    },
    "organizations": [
      {
        "id": 0,
        "name": "string",
        "priority": "Tertiary"
      }
    ],
    "fundraisers": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "teams": {
      "enabled": true,
      "defaultTargetAmount": 0,
      "allowSelfSignUp": true
    },
    "fields": {
      "Registration": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ],
      "Donation": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ],
      "Ticket": [
        {
          "identifier": "string",
          "type": "text",
          "label": "string",
          "mandatory": true
        }
      ]
    },
    "template": {
      "key": "string",
      "value": {}
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[EventElementModel](#schemaeventelementmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSlistactionresult_eventelementmodel_">ListActionResult_EventElementModel_</h2>

<a id="schemalistactionresult_eventelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "id": 0,
        "organizationId": 0,
        "organizationFee": 0,
        "name": "string",
        "createdAt": "2018-08-20T06:00:18Z",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "urlPath": "string",
        "status": "live",
        "targetAmount": 0,
        "averageDonationAmount": 0,
        "raisedAmount": 0,
        "donationCount": 0,
        "donationSetup": {
          "allowRecurringGiving": true
        },
        "organizations": [
          {
            "id": 0,
            "name": "string",
            "priority": "Tertiary"
          }
        ],
        "fundraisers": {
          "enabled": true,
          "defaultTargetAmount": 0,
          "allowSelfSignUp": true
        },
        "teams": {
          "enabled": true,
          "defaultTargetAmount": 0,
          "allowSelfSignUp": true
        },
        "fields": {
          "Registration": [
            {
              "identifier": "string",
              "type": "text",
              "label": "string",
              "mandatory": true
            }
          ],
          "Donation": [
            {
              "identifier": "string",
              "type": "text",
              "label": "string",
              "mandatory": true
            }
          ],
          "Ticket": [
            {
              "identifier": "string",
              "type": "text",
              "label": "string",
              "mandatory": true
            }
          ]
        },
        "template": {
          "key": "string",
          "value": {}
        }
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_EventElementModel_](#schemapagedlist_eventelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_eventelementmodel_">PagedList_EventElementModel_</h2>

<a id="schemapagedlist_eventelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "id": 0,
      "organizationId": 0,
      "organizationFee": 0,
      "name": "string",
      "createdAt": "2018-08-20T06:00:18Z",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "urlPath": "string",
      "status": "live",
      "targetAmount": 0,
      "averageDonationAmount": 0,
      "raisedAmount": 0,
      "donationCount": 0,
      "donationSetup": {
        "allowRecurringGiving": true
      },
      "organizations": [
        {
          "id": 0,
          "name": "string",
          "priority": "Tertiary"
        }
      ],
      "fundraisers": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "teams": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "fields": {
        "Registration": [
          {
            "identifier": "string",
            "type": "text",
            "label": "string",
            "mandatory": true
          }
        ],
        "Donation": [
          {
            "identifier": "string",
            "type": "text",
            "label": "string",
            "mandatory": true
          }
        ],
        "Ticket": [
          {
            "identifier": "string",
            "type": "text",
            "label": "string",
            "mandatory": true
          }
        ]
      },
      "template": {
        "key": "string",
        "value": {}
      }
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[EventElementModel](#schemaeventelementmodel)]|false|none|none|

<h2 id="tocSscalaractionresult_fundraiserelementmodel_">ScalarActionResult_FundraiserElementModel_</h2>

<a id="schemascalaractionresult_fundraiserelementmodel_"></a>

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "averageDonationAmount": 0,
    "campaignId": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "manager": {
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "id": 0
    },
    "name": "string",
    "newsletter": true,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "phoneNumber": "string",
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "teamId": 0,
    "team": {
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "template": {
      "key": "string",
      "value": {}
    },
    "urlPath": "string",
    "url": "string",
    "urlFull": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[FundraiserElementModel](#schemafundraiserelementmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSscalaractionresult_fundraiserpublicmodel_">ScalarActionResult_FundraiserPublicModel_</h2>

<a id="schemascalaractionresult_fundraiserpublicmodel_"></a>

```json
{
  "data": {
    "averageDonationAmount": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "raisedAmount": 0,
    "status": "live",
    "targetAmount": 0,
    "team": {
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "targetAmount": 0,
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "template": {
      "value": {
        "property1": {},
        "property2": {}
      }
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[FundraiserPublicModel](#schemafundraiserpublicmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSlistactionresult_fundraiserelementmodel_">ListActionResult_FundraiserElementModel_</h2>

<a id="schemalistactionresult_fundraiserelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "address": {
          "street": "string",
          "city": "string",
          "state": "string",
          "postcode": "string",
          "country": "string"
        },
        "averageDonationAmount": 0,
        "campaignId": 0,
        "campaign": {
          "allowsFundraisers": true,
          "allowsFundraiserSelfSignUp": true,
          "allowsTeams": true,
          "allowsTeamSelfSignUp": true,
          "donationCount": 0,
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "raisedAmount": 0,
          "status": "live",
          "targetAmount": 0,
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "donationCount": 0,
        "id": 0,
        "isPublic": true,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "manager": {
          "email": "string",
          "firstName": "string",
          "lastName": "string",
          "id": 0
        },
        "name": "string",
        "newsletter": true,
        "organization": {
          "country": "string",
          "currency": "string",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "phoneNumber": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "teamId": 0,
        "team": {
          "donationCount": 0,
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "raisedAmount": 0,
          "targetAmount": 0,
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "template": {
          "key": "string",
          "value": {}
        },
        "urlPath": "string",
        "url": "string",
        "urlFull": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_FundraiserElementModel_](#schemapagedlist_fundraiserelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_fundraiserelementmodel_">PagedList_FundraiserElementModel_</h2>

<a id="schemapagedlist_fundraiserelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "averageDonationAmount": 0,
      "campaignId": 0,
      "campaign": {
        "allowsFundraisers": true,
        "allowsFundraiserSelfSignUp": true,
        "allowsTeams": true,
        "allowsTeamSelfSignUp": true,
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "template": {
          "key": "string",
          "value": {}
        },
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "id": 0,
      "isPublic": true,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "manager": {
        "email": "string",
        "firstName": "string",
        "lastName": "string",
        "id": 0
      },
      "name": "string",
      "newsletter": true,
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "template": {
          "key": "string",
          "value": {}
        },
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "phoneNumber": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "teamId": 0,
      "team": {
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "targetAmount": 0,
        "template": {
          "key": "string",
          "value": {}
        },
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "template": {
        "key": "string",
        "value": {}
      },
      "urlPath": "string",
      "url": "string",
      "urlFull": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[FundraiserElementModel](#schemafundraiserelementmodel)]|false|none|none|

<h2 id="tocSscalaractionresult_organizationelementmodel_">ScalarActionResult_OrganizationElementModel_</h2>

<a id="schemascalaractionresult_organizationelementmodel_"></a>

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "currency": "string",
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "fundraisingPageCreatedEmail": "string",
    "id": 0,
    "legalName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "newDonationEmail": "string",
    "newInvoiceEmail": "string",
    "paymentPlatforms": [
      {
        "id": 0,
        "type": "creditCardForm",
        "platform": "stripe"
      }
    ],
    "taxId": "string",
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[OrganizationElementModel](#schemaorganizationelementmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSscalaractionresult_organizationpublicmodel_">ScalarActionResult_OrganizationPublicModel_</h2>

<a id="schemascalaractionresult_organizationpublicmodel_"></a>

```json
{
  "data": {
    "country": "string",
    "currency": "string",
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "id": 0,
    "name": "string",
    "legalName": "string",
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "template": {
      "key": "string",
      "value": {}
    },
    "timezone": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[OrganizationPublicModel](#schemaorganizationpublicmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSlistactionresult_organizationelementmodel_">ListActionResult_OrganizationElementModel_</h2>

<a id="schemalistactionresult_organizationelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "address": {
          "street": "string",
          "city": "string",
          "state": "string",
          "postcode": "string",
          "country": "string"
        },
        "currency": "string",
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "fundraisingPageCreatedEmail": "string",
        "id": 0,
        "legalName": "string",
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "newDonationEmail": "string",
        "newInvoiceEmail": "string",
        "paymentPlatforms": [
          {
            "id": 0,
            "type": "creditCardForm",
            "platform": "stripe"
          }
        ],
        "taxId": "string",
        "template": {
          "key": "string",
          "value": {}
        },
        "timezone": "string",
        "urlFull": "string",
        "urlPath": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_OrganizationElementModel_](#schemapagedlist_organizationelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_organizationelementmodel_">PagedList_OrganizationElementModel_</h2>

<a id="schemapagedlist_organizationelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "currency": "string",
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "fundraisingPageCreatedEmail": "string",
      "id": 0,
      "legalName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "newDonationEmail": "string",
      "newInvoiceEmail": "string",
      "paymentPlatforms": [
        {
          "id": 0,
          "type": "creditCardForm",
          "platform": "stripe"
        }
      ],
      "taxId": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "timezone": "string",
      "urlFull": "string",
      "urlPath": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[OrganizationElementModel](#schemaorganizationelementmodel)]|false|none|none|

<h2 id="tocSscalaractionresult_pagepublicgeneralmodel_">ScalarActionResult_PagePublicGeneralModel_</h2>

<a id="schemascalaractionresult_pagepublicgeneralmodel_"></a>

```json
{
  "data": {
    "type": "organization",
    "campaign": {
      "additionalDonationsNeededForTarget": 0,
      "averageDonationAmount": 0,
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "dataCapture": {
        "registration": {
          "phone": {
            "capture": true,
            "mandatory": true
          },
          "address": {
            "capture": true,
            "mandatory": true
          }
        },
        "donation": {
          "phone": {
            "capture": true,
            "mandatory": true
          },
          "address": {
            "capture": true,
            "mandatory": true
          }
        }
      },
      "donationCount": 0,
      "donationSetup": {
        "allowRecurringGiving": true
      },
      "fundraisersCount": 0,
      "fundraisers": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organizationId": 0,
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "pagesCount": 0,
      "paymentPlatforms": {
        "main": {
          "id": 0,
          "platform": "stripe",
          "platformType": "creditCardForm",
          "publicKey": "string"
        },
        "alternative": [
          {
            "id": 0,
            "platform": "stripe",
            "platformType": "creditCardForm",
            "publicKey": "string"
          }
        ]
      },
      "raisedAmount": 0,
      "targetAmount": 0,
      "type": "default",
      "status": "live",
      "teamsCount": 0,
      "teams": {
        "enabled": true,
        "defaultTargetAmount": 0,
        "allowSelfSignUp": true
      },
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "fundraiser": {
      "averageDonationAmount": 0,
      "campaign": {
        "allowsFundraisers": true,
        "allowsFundraiserSelfSignUp": true,
        "allowsTeams": true,
        "allowsTeamSelfSignUp": true,
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "id": 0,
      "isPublic": true,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "team": {
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "template": {
        "value": {
          "property1": {},
          "property2": {}
        }
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "organization": {
      "country": "string",
      "currency": "string",
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "id": 0,
      "name": "string",
      "legalName": "string",
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "timezone": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "team": {
      "averageDonationAmount": 0,
      "campaign": {
        "allowsFundraisers": true,
        "allowsFundraiserSelfSignUp": true,
        "allowsTeams": true,
        "allowsTeamSelfSignUp": true,
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "id": 0,
      "isPublic": true,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "raisedAmount": 0,
      "status": "live",
      "fundraisersCount": 0,
      "targetAmount": 0,
      "template": {
        "value": {
          "property1": {},
          "property2": {}
        }
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    }
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagePublicGeneralModel](#schemapagepublicgeneralmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSlistactionresult_pageelementmodel_">ListActionResult_PageElementModel_</h2>

<a id="schemalistactionresult_pageelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "accountId": 0,
        "account": {
          "id": 0,
          "email": "string",
          "firstName": "string",
          "lastName": "string"
        },
        "additionalDonationsNeededForTarget": 0,
        "averageDonationAmount": 0,
        "campaignId": 0,
        "campaign": {
          "name": "string",
          "status": "live",
          "template": {
            "key": "string",
            "value": {}
          },
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "urlPath": "string"
        },
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "donationCount": 0,
        "eventId": 0,
        "event": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "fundraiserId": 0,
        "fundraiser": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "isFundraiserOrTeam": true,
        "isActive": true,
        "isPublic": true,
        "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
        "lastUpdatedAt": "2018-08-20T06:00:18Z",
        "name": "string",
        "newsletterOptIn": true,
        "organizationId": 0,
        "organization": {
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "phoneNumber": "string",
        "raisedAmount": 0,
        "status": "string",
        "targetAmount": 0,
        "teamId": 0,
        "team": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "type": "campaign",
        "urlPath": "string",
        "url": "string",
        "urlFull": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_PageElementModel_](#schemapagedlist_pageelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_pageelementmodel_">PagedList_PageElementModel_</h2>

<a id="schemapagedlist_pageelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "accountId": 0,
      "account": {
        "id": 0,
        "email": "string",
        "firstName": "string",
        "lastName": "string"
      },
      "additionalDonationsNeededForTarget": 0,
      "averageDonationAmount": 0,
      "campaignId": 0,
      "campaign": {
        "name": "string",
        "status": "live",
        "template": {
          "key": "string",
          "value": {}
        },
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "urlPath": "string"
      },
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "eventId": 0,
      "event": {
        "status": "live",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "urlPath": "string"
      },
      "fundraiserId": 0,
      "fundraiser": {
        "status": "live",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "urlPath": "string"
      },
      "isFundraiserOrTeam": true,
      "isActive": true,
      "isPublic": true,
      "lastUpdatedAtLocal": "2018-08-20T06:00:18Z",
      "lastUpdatedAt": "2018-08-20T06:00:18Z",
      "name": "string",
      "newsletterOptIn": true,
      "organizationId": 0,
      "organization": {
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "urlPath": "string"
      },
      "phoneNumber": "string",
      "raisedAmount": 0,
      "status": "string",
      "targetAmount": 0,
      "teamId": 0,
      "team": {
        "status": "live",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "urlPath": "string"
      },
      "type": "campaign",
      "urlPath": "string",
      "url": "string",
      "urlFull": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[PageElementModel](#schemapageelementmodel)]|false|none|none|

<h2 id="tocSlistactionresult_pagepublicmodel_">ListActionResult_PagePublicModel_</h2>

<a id="schemalistactionresult_pagepublicmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "additionalDonationsNeededForTarget": 0,
        "averageDonationAmount": 0,
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "campaignId": 0,
        "campaign": {
          "name": "string",
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "urlPath": "string"
        },
        "donationCount": 0,
        "event": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "fundraiserId": 0,
        "fundraiser": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "name": "string",
        "organizationId": 0,
        "organization": {
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "raisedAmount": 0,
        "status": "string",
        "targetAmount": 0,
        "teamId": 0,
        "team": {
          "status": "live",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "urlPath": "string"
        },
        "type": "campaign",
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_PagePublicModel_](#schemapagedlist_pagepublicmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_pagepublicmodel_">PagedList_PagePublicModel_</h2>

<a id="schemapagedlist_pagepublicmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "additionalDonationsNeededForTarget": 0,
      "averageDonationAmount": 0,
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "campaignId": 0,
      "campaign": {
        "name": "string",
        "status": "live",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "urlPath": "string"
      },
      "donationCount": 0,
      "event": {
        "status": "live",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "urlPath": "string"
      },
      "fundraiserId": 0,
      "fundraiser": {
        "status": "live",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "urlPath": "string"
      },
      "name": "string",
      "organizationId": 0,
      "organization": {
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "urlPath": "string"
      },
      "raisedAmount": 0,
      "status": "string",
      "targetAmount": 0,
      "teamId": 0,
      "team": {
        "status": "live",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "urlPath": "string"
      },
      "type": "campaign",
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[PagePublicModel](#schemapagepublicmodel)]|false|none|none|

<h2 id="tocSscalaractionresult_sessionelementmodel_">ScalarActionResult_SessionElementModel_</h2>

<a id="schemascalaractionresult_sessionelementmodel_"></a>

```json
{
  "data": {
    "key": "string",
    "account": {
      "id": 0,
      "firstName": "string",
      "lastName": "string",
      "source": "default"
    },
    "organization": {
      "id": 0,
      "name": "string"
    },
    "expiry": "2018-08-20T06:00:18Z",
    "impersonated": true,
    "impersonator": {
      "id": 0,
      "firstName": "string",
      "lastName": "string",
      "source": "default"
    },
    "isFundraiser": true,
    "isSystemAdmin": true,
    "isOrganizationAdmin": true,
    "refresh": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[SessionElementModel](#schemasessionelementmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSscalaractionresult_teamelementmodel_">ScalarActionResult_TeamElementModel_</h2>

<a id="schemascalaractionresult_teamelementmodel_"></a>

```json
{
  "data": {
    "address": {
      "street": "string",
      "city": "string",
      "state": "string",
      "postcode": "string",
      "country": "string"
    },
    "averageDonationAmount": 0,
    "campaignId": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "manager": {
      "email": "string",
      "firstName": "string",
      "lastName": "string",
      "id": 0
    },
    "name": "string",
    "newsletter": true,
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "phoneNumber": "string",
    "raisedAmount": 0,
    "status": "live",
    "fundraisersActiveCount": 0,
    "fundraisersCount": 0,
    "targetAmount": 0,
    "template": {
      "key": "string",
      "value": {}
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[TeamElementModel](#schemateamelementmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSscalaractionresult_teampublicmodel_">ScalarActionResult_TeamPublicModel_</h2>

<a id="schemascalaractionresult_teampublicmodel_"></a>

```json
{
  "data": {
    "averageDonationAmount": 0,
    "campaign": {
      "allowsFundraisers": true,
      "allowsFundraiserSelfSignUp": true,
      "allowsTeams": true,
      "allowsTeamSelfSignUp": true,
      "donationCount": 0,
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "raisedAmount": 0,
      "status": "live",
      "targetAmount": 0,
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "createdAtLocal": "2018-08-20T06:00:18Z",
    "createdAt": "2018-08-20T06:00:18Z",
    "donationCount": 0,
    "id": 0,
    "isPublic": true,
    "mainImagePath": "string",
    "mainImageUrl": "string",
    "name": "string",
    "organization": {
      "country": "string",
      "currency": "string",
      "id": 0,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "name": "string",
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    },
    "raisedAmount": 0,
    "status": "live",
    "fundraisersCount": 0,
    "targetAmount": 0,
    "template": {
      "value": {
        "property1": {},
        "property2": {}
      }
    },
    "url": "string",
    "urlFull": "string",
    "urlPath": "string"
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[TeamPublicModel](#schemateampublicmodel)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSlistactionresult_teamelementmodel_">ListActionResult_TeamElementModel_</h2>

<a id="schemalistactionresult_teamelementmodel_"></a>

```json
{
  "data": {
    "totalCount": 0,
    "page": 0,
    "pageSize": 0,
    "list": [
      {
        "address": {
          "street": "string",
          "city": "string",
          "state": "string",
          "postcode": "string",
          "country": "string"
        },
        "averageDonationAmount": 0,
        "campaignId": 0,
        "campaign": {
          "allowsFundraisers": true,
          "allowsFundraiserSelfSignUp": true,
          "allowsTeams": true,
          "allowsTeamSelfSignUp": true,
          "donationCount": 0,
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "raisedAmount": 0,
          "status": "live",
          "targetAmount": 0,
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "createdAtLocal": "2018-08-20T06:00:18Z",
        "createdAt": "2018-08-20T06:00:18Z",
        "donationCount": 0,
        "id": 0,
        "isPublic": true,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "manager": {
          "email": "string",
          "firstName": "string",
          "lastName": "string",
          "id": 0
        },
        "name": "string",
        "newsletter": true,
        "organization": {
          "country": "string",
          "currency": "string",
          "id": 0,
          "mainImagePath": "string",
          "mainImageUrl": "string",
          "name": "string",
          "template": {
            "key": "string",
            "value": {}
          },
          "url": "string",
          "urlFull": "string",
          "urlPath": "string"
        },
        "phoneNumber": "string",
        "raisedAmount": 0,
        "status": "live",
        "fundraisersActiveCount": 0,
        "fundraisersCount": 0,
        "targetAmount": 0,
        "template": {
          "key": "string",
          "value": {}
        },
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      }
    ]
  },
  "success": true,
  "error": [
    {
      "error": "string",
      "param": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[PagedList_TeamElementModel_](#schemapagedlist_teamelementmodel_)|false|none|none|
|success|boolean|false|none|none|
|error|[[ErrorResult](#schemaerrorresult)]|false|none|none|

<h2 id="tocSpagedlist_teamelementmodel_">PagedList_TeamElementModel_</h2>

<a id="schemapagedlist_teamelementmodel_"></a>

```json
{
  "totalCount": 0,
  "page": 0,
  "pageSize": 0,
  "list": [
    {
      "address": {
        "street": "string",
        "city": "string",
        "state": "string",
        "postcode": "string",
        "country": "string"
      },
      "averageDonationAmount": 0,
      "campaignId": 0,
      "campaign": {
        "allowsFundraisers": true,
        "allowsFundraiserSelfSignUp": true,
        "allowsTeams": true,
        "allowsTeamSelfSignUp": true,
        "donationCount": 0,
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "raisedAmount": 0,
        "status": "live",
        "targetAmount": 0,
        "template": {
          "key": "string",
          "value": {}
        },
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "createdAtLocal": "2018-08-20T06:00:18Z",
      "createdAt": "2018-08-20T06:00:18Z",
      "donationCount": 0,
      "id": 0,
      "isPublic": true,
      "mainImagePath": "string",
      "mainImageUrl": "string",
      "manager": {
        "email": "string",
        "firstName": "string",
        "lastName": "string",
        "id": 0
      },
      "name": "string",
      "newsletter": true,
      "organization": {
        "country": "string",
        "currency": "string",
        "id": 0,
        "mainImagePath": "string",
        "mainImageUrl": "string",
        "name": "string",
        "template": {
          "key": "string",
          "value": {}
        },
        "url": "string",
        "urlFull": "string",
        "urlPath": "string"
      },
      "phoneNumber": "string",
      "raisedAmount": 0,
      "status": "live",
      "fundraisersActiveCount": 0,
      "fundraisersCount": 0,
      "targetAmount": 0,
      "template": {
        "key": "string",
        "value": {}
      },
      "url": "string",
      "urlFull": "string",
      "urlPath": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalCount|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|
|pageSize|integer(int32)|false|none|none|
|list|[[TeamElementModel](#schemateamelementmodel)]|false|none|none|

