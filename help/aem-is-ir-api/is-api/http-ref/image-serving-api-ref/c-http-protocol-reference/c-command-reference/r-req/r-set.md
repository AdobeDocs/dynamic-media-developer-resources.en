---
description: Media set info.
seo-description: Media set info.
seo-title: set
solution: Experience Manager
title: set
uuid: ebd78249-45ea-47cd-8845-786070f92f21
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# set{#set}

Media set info.

req=set[,xml[, *`encoding`*]|{json[&id= *`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> encoding</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Unique request identifier </p></td> 
 </tr> 
</table>

Returns information about images, videos, swatches, and various metadata associated with catalog::ImageSet for the image catalog entry specified in the URL path. This response is a hierarchical structure as determined by the type of set provided. Appropriate formatting is applied when 'xml' or 'json' format is requested.

The HTTP response is cacheable with the TTL based on `catalog::NonImgExpiration`.

>[!NOTE]
>
>The colon character is not allowed in req=set requests.

Requests that support JSON response format lets you specify the name of the JS callback handler using the extended syntax of `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is the name of JS handler present in the JSONP response. Only a-z, A-Z, and 0-9 characters are allowed. Optional. Default is `s7jsonResponse`. 
