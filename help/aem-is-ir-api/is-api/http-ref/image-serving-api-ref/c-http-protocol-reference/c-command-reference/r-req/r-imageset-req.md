---
description: Image set data from image catalog. Returns image set data for the image catalog entry specified in the URL path.
seo-description: Image set data from image catalog. Returns image set data for the image catalog entry specified in the URL path.
seo-title: imageset
solution: Experience Manager
title: imageset
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
feature: "Dynamic Media Classic,SDK/API,Image Sets"
role: "Developer,Business Practitioner"
---

# imageset{#imageset}

Image set data from image catalog. Returns image set data for the image catalog entry specified in the URL path.

 `req=imageset[,text|javascript|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Unique request identifier. </p></td> 
 </tr> 
</table>

The content of `catalog::ImageSet` is returned without further modification (except string localization, if applicable), followed by a single line terminator (CR/LF). If the URL path does not resolve to a valid catalog entry, the response consists only of a single line terminator.

Other commands in the request string are ignored. The HTTP response is cacheable with the TTL based on `catalog::NonImgExpiration`.

Requests that support JSONP response format lets you specify the name of the JS callback handler using the extended syntax of `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is the name of the JS handler that is present in the JSONP response. Only a-z, A-Z, and 0-9 characters are allowed. Optional. Default is `s7jsonResponse`. 
