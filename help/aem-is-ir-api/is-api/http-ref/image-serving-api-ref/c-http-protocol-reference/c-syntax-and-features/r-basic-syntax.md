---
description: The HTTP protocol basic syntax is as follows.
solution: Experience Manager
title: Image Serving HTTP protocol basic syntax
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
---
# Image Serving HTTP protocol basic syntax{#image-serving-http-protocol-basic-syntax}

The HTTP protocol basic syntax is as follows:

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> request</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> modifiers</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span> </span> </p></td> 
  <td class="stentry"> <p>Source object specifier (image path or image catalog entry). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifiers</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span>*[&amp;<span class="varname"> modifier</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">command|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> command</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
  <td class="stentry"> <p>Name of a command macro.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> comment</span> </span> </p></td> 
  <td class="stentry"> <p>Comment string (ignored by server).</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>One of the supported command or attribute names.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Name of a custom variable.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span> </span> </p></td> 
  <td class="stentry"> <p>Command or variable value. </p></td> 
 </tr> 
</table>

*`server_address`*, *`cmdName`*, *`macro`*, and *`var`* are case-insensitive. The server preserves the case of all other string values.

*`value`* is command-specific and can consist of one or more values separated by commas. Refer to the description of the individual commands for details.

## Server identifier {#section-926ae55ddba14b8d952147a5fd701e14}

The [!DNL /is/image] root context is required for all HTTP requests to Image Serving.

## HTTP decoding {#section-20922baccd804d2d986b44ce9a183a7d}

Image Serving first extracts *`object`* and *`modifiers`* from the incoming request. *`object`* is then separated into path elements which are individually HTTP-decoded. The *`modifiers`* string is separated into *`command`*= *`value`* pairs, and *`value`* is then HTTP-decoded before command-specific processing.

>[!NOTE]
>
>Unless otherwise noted in the documentation, all unsafe characters must be encoded per the HTTP standard. Refer to the HTTP specification for details.

## Comments {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Comments can be embedded into request strings anywhere and are identified by a period(.) immediately following the command separator(&). The comment is terminated by the next occurrence of an (unencoded) command separator. This feature can be used to add information to the request which is not for Image Serving use, such as time stamps, and database IDs.

## See also {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Data Types](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [HTTP/1.1 Specification](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
