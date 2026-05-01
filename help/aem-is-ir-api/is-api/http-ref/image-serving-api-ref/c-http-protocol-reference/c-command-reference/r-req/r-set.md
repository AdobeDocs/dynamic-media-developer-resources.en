---
description: Media set info.
solution: Experience Manager
title: set
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
TQID: https://experienceleague.adobe.com/crvaC2wnug9brH2sKb3ROECV7g4QsZm3C48LwhfexAw
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
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
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
