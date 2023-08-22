---
title: pathAttr
description: Text-on-path attributes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
---
# pathAttr{#pathattr}

Text-on-path attributes.

 ` pathAttr= *`direction`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> direction </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norm </span> | <span class="codeph"> reverse </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>Text start position on path (real 0.0…1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>Text end position on path (real 0.0…&lt;2.0). </p> </td> 
 </tr> 
</table>

Specify `norm` to draw text starting near the first path vertex and `reverse` to draw text in the opposite direction, starting near the last vertex.

*`startPos`* and *`endPos`* allow adjusting where on the path the text is drawn. 0.0 corresponds to the first vertex in the path and 1.0 to the last vertex; intermediate values express the distance along the path between the first and last vertex.

## Properties {#section-80f266da4e2549d89f022a3f9ff4584d}

Layer attribute. Ignored if the layer does not include `textPs=` and `textPath=` commands.

*`startPos`* must be greater than or equal to 0 and less than 1.0. *`endPos`* must be greater than *`startPos`* and less than or equal to 1.0 when applied to an open path, or less than or equal to ( *`startPos`* + 1.0) when applied to a closed path.

## Default {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## See also {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
