---
title: map
description: Image map data.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
---
# map{#map}

Image map data.

 `req=map[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Unique request identifier. </p></td> 
 </tr> 
</table>

Returns `catalog::Map` without modification when querying a simple catalog entry with no additional commands specified (does not scale to `catalog::maxPix`).

If any other commands are specified in the request, a composite image map is returned. The composite image map is derived by scaling, cropping, rotating, and layering all `catalog::Map` and/or `map=` commands included in the request, just like the image data would be with `req=img`.

Specify `text` or omit the second parameter so you can return the image map data in form of an `HTML <AREA>` element string with response MIME type `text/plain`.

Specify `xml` so you can format the response as XML instead of HTML. Text encoding can be specified optionally. The default is `UTF-8`.

Returns an empty string (or empty `<AREA>` element) if no map data was found for the specified catalog objects, and/or if no `<AREA>` elements remain after cropping the images.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

Requests that support JSONP response format lets you specify the name of the JS callback handler using the extended syntax of `req=` parameter:

`req=...,json [&handler = reqHandler ]`

The `<reqHandler>` is the name of the JS handler that is present in the JSONP response. Only a-z, A-Z, and 0-9 characters are allowed. Optional. The default is `s7jsonResponse`.

See [Image Maps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
