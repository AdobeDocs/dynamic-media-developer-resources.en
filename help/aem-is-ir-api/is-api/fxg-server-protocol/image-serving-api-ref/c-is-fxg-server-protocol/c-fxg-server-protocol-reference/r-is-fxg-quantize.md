---
title: quantize
description: Color quantization. Specifies color-quantization attributes for GIF output conversion.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
TQID: 'https://experienceleague.adobe.com/m5e14tLMY1JAdZTzlw7iUZzXzL9yylP66MYi5XAeYtg'
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
---
# quantize{#quantize}

Color quantization. Specifies color-quantization attributes for GIF output conversion.

 ` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> palette type </p> <p>Select ' <span class="codeph"> web </span>' or ' <span class="codeph"> mac </span>' to choose a predefined palette, or set to ' <span class="codeph"> adaptive </span>' to calculate an optimal palette for the image. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> dithering options </p> <p>Select 'diffuse' for Floyd-Steinberg error diffusion or 'off' to disable dithering. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Number of output colors (integer) included in the ' <span class="codeph"> adaptive </span>' palette. </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> must be from 2 through 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Comma-separated list of forced RGB colors in hex6 format. Lets you specify forced colors to be included in an ' <span class="codeph"> adaptive </span>' palette. If the number of colors specified is less than <span class="codeph"> numColors </span>, additional colors are calculated based on the image content. </p> <p>Used only if <span class="codeph"> fmt=gif </span> or <span class="codeph"> fmt=gif-alpha </span>. Ignored otherwise. The colors specified with <span class="codeph"> <span class="varname"> colorList </span> </span> must be RGB values in hex6 format (see <span class="codeph"> color </span>); no other color specifiers are permitted. </p> </td> 
 </tr> 
</table>

## Default {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Example {#section-b3a979dc9ae3459baa093bf17310988f}

Generate a GIF thumbnail using the ' `web`' palette and no dithering:

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

Convert the image to a bi-tonal GIF with key-color transparency and force colors to black and white:

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
