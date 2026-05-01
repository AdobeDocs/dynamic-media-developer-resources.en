---
title: JSONP properties
description: If jsonp is specified as the response format, the reply data is formatted using JSONP (JavaScript Object Notation with Padding), wrapped in a JavaScript function call.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
TQID: https://experienceleague.adobe.com/UOLxt6u-df-sDOl5ZozTtSKa6r-q2LFR1PyFO1IGnkg
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# JSONP properties{#jsonp-properties}

If jsonp is specified as the response format, the reply data is formatted using JSONP (JavaScript Object Notation with Padding), wrapped in a JavaScript function call.

 The client may specify an optional unique request identifier ( *`reqId`*), which is returned in the response and allows the client to distinguish multiple responses received asynchronously. A typical response has the following general structure:

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

The `s7jsonResponse` JavaScript function must be defined by the client. In its simplest form, the function might look like this:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Requests that support JSONP response format lets you specify the name of the JS callback handler using the extended syntax of `req=` parameter:

`req=...,json [&handler = reqHandler]`

The `<reqHandler>` syntax is the name of the JS handler that is present in the JSONP response. Only a-z, A-Z, and 0-9 characters are allowed. Optional. Default is `s7jsonResponse`.

The Dynamic Media Image Serving Viewers package includes a utility to request and parse JSONP-formatted data from Image Serving.

See [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) for more information about the JSONP format.

See [www.json.org](https://www.json.org/json-en.html) for more information about the JSON format.

See also [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
