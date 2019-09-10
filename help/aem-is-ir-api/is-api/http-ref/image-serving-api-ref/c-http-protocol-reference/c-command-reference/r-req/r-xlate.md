---
description: Available locale-specific versions. Returns a list of available locale-specific versions of the catalog id specified in the request path.
seo-description: Available locale-specific versions. Returns a list of available locale-specific versions of the catalog id specified in the request path.
seo-title: xlate
solution: Experience Manager
title: xlate
topic: Scene7 Image Serving - Image Rendering API
uuid: 4c2370e5-1d46-4242-89bb-a5ce416ef63c
index: y
internal: n
snippet: y
---

# xlate{#xlate}

Available locale-specific versions. Returns a list of available locale-specific versions of the catalog id specified in the request path.

 `req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Unique request identifier. </p></td> 
 </tr> 
</table>

See [Object Id Translation](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

For example:

`xlate.translatedIds=image,image_fr,image_de`

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

Requests that support JSONP response format lets you specify the name of the JS callback handler using the extended syntax of `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is the name of the JS handler that is present in the JSONP response. Only a-z, A-Z, and 0-9 characters are allowed. Optional. Default is `s7jsonResponse`. 
