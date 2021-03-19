---
description: User data from image catalog. Returns user data for the image catalog entry specified in the url path.
seo-description: User data from image catalog. Returns user data for the image catalog entry specified in the url path.
seo-title: userdata
solution: Experience Manager
title: userdata
uuid: 7a34adad-f1b6-45a7-94fe-1407845710e5
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# userdata{#userdata}

User data from image catalog. Returns user data for the image catalog entry specified in the url path.

 `req=userdata[,text|{xml[, *`encoding`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> encoding</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

The contents of `catalog::UserData` are returned. When 'text' format is specified, all instances of `??` in `catalog::UserData`are replaced by line terminators, and a single line terminator (CR/LF) is appended to the end. If the URL path does not resolve to a valid catalog entry, the response consists only of a single line terminator. Appropriate formatting is applied when 'xml' or 'json' format is requested.

Other commands in the request string are ignored.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

>[!NOTE]
>
>The colon character is not allowed in userdata property key names.

Requests that support JSONP response format lets you specify the name of the JS callback handler using the extended syntax of `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` is the name of the JS handler that is present in the JSONP response. Only a-z, A-Z, and 0-9 characters are allowed. Optional. Default is `s7jsonResponse`. 
