---
description: Image exists.
seo-description: Image exists.
seo-title: exists
solution: Experience Manager
title: exists
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# exists{#exists}

Image exists.

 `req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* unique request identifier

Returns a single property named `catalogRecord.exists`. The property value is set to "1" if the specified catalog entry exists in the image or default catalog, otherwise it is set to "0". `req=exists` requests against the `/is/content` context will indicate the presence or absence of a specified record in the static content catalog.

Other commands in the request string are ignored. The HTTP response is cacheable with the TTL based on `attribute::NonImgExpiration`.

Requests that support JSONP response format lets you specify the name of the JS callback handler using the extended syntax of `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is the name of the JS handler that is present in the JSONP response. Only a-z, A-Z, and 0-9 characters are allowed. Optional. Default is `s7jsonResponse`. 
