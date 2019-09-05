---
description: If jsonp is specified as the response format, the reply data is formatted using JSONP (JavaScript Object Notation with Padding), wrapped in a JavaScript function call.
seo-description: If jsonp is specified as the response format, the reply data is formatted using JSONP (JavaScript Object Notation with Padding), wrapped in a JavaScript function call.
seo-title: JSONP properties
solution: Experience Manager
title: JSONP properties
topic: Scene7 Image Serving - Image Rendering API
uuid: 2679d8b0-b74c-4d80-a755-fe0909694eaf
index: y
internal: n
snippet: y
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

`<reqHandler>` is the name of the JS handler that is present in the JSONP response. Only a-z, A-Z, and 0-9 characters are allowed. Optional. Default is `s7jsonResponse`.

The Scene7 Image Serving Viewers package includes a utility to request and parse JSONP-formatted data from Image Serving.

See [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) for more information about the JSONP format.

See [www.json.org](http://www.json.org) for more information about the JSON format.

See also [req](../../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76). 
