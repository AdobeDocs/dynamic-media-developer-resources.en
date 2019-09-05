---
description: Request validation.
seo-description: Request validation.
seo-title: validate
solution: Experience Manager
title: validate
topic: Scene7 Image Serving - Image Rendering API
uuid: 8221f05a-c84b-4a05-a9ce-1872f7385c53
index: y
internal: n
snippet: y
---

# validate{#validate}

Request validation.

 `req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Unique request identifier. </p></td> 
 </tr> 
</table>

Parses the request string as if `req=img` were specified, but without substituting variables and evaluating referenced objects (images, ICC profiles, fonts, and so forth). The standard error response is returned if parsing fails, otherwise the following property is returned:

`request.isValid=1`

The HTTP response is not cacheable.

Requests that support JSONP response format lets you specify the name of the JS callback handler using the extended syntax of `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is the name of the JS handler that is present in the JSONP response. Only a-z, A-Z, and 0-9 characters are allowed. Optional. Default is `s7jsonResponse`. 
