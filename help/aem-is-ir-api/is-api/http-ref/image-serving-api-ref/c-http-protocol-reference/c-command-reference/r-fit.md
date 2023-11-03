---
title: fit
description: Response Image Fit Mode. Specifies how the scale factor is calculated, which is used to scale the composite image to the response image when the response size is specified with wid= and hei= and scl= is not present.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
---
# fit{#fit}

Response Image Fit Mode. Specifies how the scale factor is calculated, which is used to scale the composite image to the response image when the response size is specified with wid= and hei= and scl= is not present.

 ` fit= *`mode`*, *`upscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mode </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|crop|wrap|stretch|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> upscale </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

In the following description of the mode options, it is assumed that *`xScale`* is the ratio of the composite image width to the response image width and *`yScale`* is the ratio of the composite image height to the response image height.

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter </th> 
   <th colname="col2" class="entry"> Definition </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> fit </span> </p> </td> 
   <td colname="col2"> <p>Scales the composite image so that it fits into the space allocated with <span class="codeph"> wid= </span> and <span class="codeph"> hei= </span>, with minimal whitespace and no cropping. The response image has the exact size specified with <span class="codeph"> wid= </span> and <span class="codeph"> hei= </span>. The smaller of <span class="varname"> xScale </span> and <span class="varname"> yScale </span> is applied. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> constrain </span> </p> </td> 
   <td colname="col2"> <p>Scales the composite image like <span class="codeph"> fit </span> so that it fits into the space allocated with <span class="codeph"> wid= </span> and <span class="codeph"> hei= </span>, but the actual response image may be smaller than specified with <span class="codeph"> wid= </span> and <span class="codeph"> hei= </span> to avoid whitespace. The smaller of <span class="varname"> xScale </span> and <span class="varname"> yScale </span> is applied. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> crop </span> </p> </td> 
   <td colname="col2"> <p>Scales the composite image so that it fills the entire response image, with minimal cropping and no whitespace. The larger of <span class="varname"> xScale </span> and <span class="varname"> yScale </span> is applied. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> wrap </span> </p> </td> 
   <td colname="col2"> <p>Scales the composite image like <span class="codeph"> crop </span> so that it covers the entire response image, but the actual response image may be larger than specified with <span class="codeph"> wid= </span> and <span class="codeph"> hei= </span> to avoid cropping. The larger of <span class="varname"> xScale </span> and <span class="varname"> yScale </span>is applied. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> stretch </span> </p> </td> 
   <td colname="col2"> <p>Scales the composite image independently in x and y to fill the entire response image, with no cropping and no whitespace. This typically changes the aspect ratio of the image. <span class="varname"> xScale </span> is used for horizontal scaling and <span class="varname"> yScale </span> for vertical scaling. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>Applies <span class="varname"> xScale </span> to tightly fit the image horizontally, with likely cropping or whitespace at the top and/or bottom. Useful for special applications. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>Applies <span class="varname"> yScale </span> to tightly fit the image vertically, with likely cropping or whitespace at the left and/or right. Useful for special applications. </p> </td> 
  </tr> 
 </tbody> 
</table>

Set *`upscale`* to '1' to allow upscaling or to '0' to constrain *`xScale`*and *`yScale`* to be limited to 1:1. If upscaling is disabled, additional whitespace may be present if the composite image is smaller than the response image.

Crop and whitespace are centered by default; their position can be controlled with `align=`. The color and opacity of the whitespace fill is determined by `bgc=`.

## Properties {#section-6d7a5a7e18434bca9bc2fdb236af8909}

View attribute. Applies regardless of the current layer setting. At least one of `wid=` or `hei=` must also be specified, otherwise an error is returned; both `wid=` and `hei=` must be specified for the fit modes to behave as described. An error is returned when `req=tmb` is specified as well.

## Default {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## See also {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
