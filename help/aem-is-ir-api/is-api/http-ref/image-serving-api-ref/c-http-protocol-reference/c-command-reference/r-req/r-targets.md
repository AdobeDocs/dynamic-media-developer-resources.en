---
description: Zoom targets data from image catalog. Returns zoom target data for the image catalog entry specified in the URL path.
solution: Experience Manager
title: targets
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
---
# targets{#targets}

Zoom targets data from image catalog. Returns zoom target data for the image catalog entry specified in the URL path.

 `req=targets[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Unique request identifier. </p></td> 
 </tr> 
</table>

The contents of `catalog::Targets` are returned. When 'text' format is requested, all instances of `??` in `catalog::Targets` are replaced by line terminators, and a single line terminator ( `CR/LF`) is appended to the end. If the URL path does not resolve to a valid catalog entry, the response consists only of a single line terminator. Appropriate formatting is applied when 'xml' or 'json' format is requested.

Other commands in the request string are ignored.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

Requests that support JSONP response format lets you specify the name of the JS callback handler using the extended syntax of `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is the name of the JS handler that is present in the JSONP response. Only a-z, A-Z, and 0-9 characters are allowed. Optional. Default is `s7jsonResponse`.
