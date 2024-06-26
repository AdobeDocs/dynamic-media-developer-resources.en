---
title: quantize
description: Color quantization. Specifies color-quantization attributes for GIF output conversion.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71d59961-848e-4d78-875e-066e842ac1bf
---
# quantize{#quantize}

Color quantization. Specifies color-quantization attributes for GIF output conversion.

 ` quantize= *`type`*[, *`dither`*[, *`numColors`*[, *`colorList`*]]]`

<table id="table_A669A9058C8043A5BAE80B03A13B015B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {adaptive|web|mac} </span> </p> <p>Specifies the palette type. </p> <p>Set to <span class="codeph"> adaptive </span> to calculate an optimal palette for the image. </p> <p>Set to <span class="codeph"> web </span> or <span class="codeph"> mac </span> to choose a pre-defined palette. </p> <p> <p>Note:  The <span class="codeph"> mac </span> pallet type is only supported for GIF and PNG8 formats but not for GIF-Alpha and PNG8-Alpha formats.</p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dither </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {diffuse|off} </span> </p> <p>Specifies the dithering options. </p> <p>Set to <span class="codeph"> diffuse </span> for Floyd-Steinberg error diffusion </p> <p>Set to <span class="codeph"> off </span> to disable dithering.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
   <td colname="col2"> <p>Number of output colors (2-256) </p> <p>Specifies how many colors are included in the <span class="codeph"> adaptive </span> palette.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
   <td colname="col2"> <p>A comma-separated list of forced RGB colors in hex6 format </p> <p>Lets you specify the colors to include in an <span class="codeph"> adaptive </span> palette. If the number of colors specified is less than <span class="codeph"> <span class="varname"> numColors </span> </span>, additional colors are calculated based on the image content.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-8ab5035055b24b858270d260912a7f3d}

Request attribute. It applies regardless of the current layer setting. Used only if `fmt=gif`, `fmt=gif-alpha`, `fmt=png8`, or `fmt=png8-alpha`. Ignored otherwise.

The colors specified with *`colorList`* must consist of RGB values in hex6 format (see [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md) without `0x` prefix. No other color specifiers are permitted. The modifier *`numColors`* must be 2&ndash;256.

## Default {#section-ca3e817617244e8798ccff67b2023a32}

`quantize=adaptive,diffuse,256`

## Example {#section-e34aca7587d548a7ae9d4266b80c9451}

Generate a GIF thumbnail using the `web` palette and no dithering:

`http:// *`*Server*`*/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`

Convert the image to a bi-tonal GIF with key-color transparency. And, force colors to black and white:

`http:// *`*Server*`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

## See also {#section-ea5e8de6084540cf86010370a4d0f01f}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
