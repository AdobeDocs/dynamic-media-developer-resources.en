---
description: Crop Image. Specifies a rectangular crop region, expressed either in pixels or normalized relative to the full-resolution source image or mask image.
solution: Experience Manager
title: crop
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
---
# crop{#crop}

Crop Image. Specifies a rectangular crop region, expressed either in pixels or normalized relative to the full-resolution source image or mask image.

 `crop= *`coord`*, *`size`*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>Pixel offset from the top-left corner of the source image to the top-left of the crop rect (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Normalized offset from the top-left of the source image to the top-left of the crop rect (real, real). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> size</span></span> </p></td> 
  <td class="stentry"> <p>Size of the crop rect in pixels (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Normalized size of the crop rect relative to the size of the source image (real, real). </p></td> 
 </tr> 
</table>

May also be used to extend the image beyond its boundaries by specifying negative x, y values and/or width, height values larger than the image width, height. In this case, the extended area is fully transparent (unless `bgColor=` is specified).

## Properties {#section-632e0405bb9940679b5f8b1c10e0902e}

Source image/mask attribute. Applies to the layer 0 source image if `layer=comp`. Ignored by layers which are not associated with a source image or mask.

## Default {#section-41f62d386c664f77952bc22e7286bb88}

Entire image ( `cropN=0,0,1,1`).

## Examples {#section-2c99b481c0a04321979a3b522aa295d1}

**Crop 10% off the left and 10% off the right:**

`…&cropN=0.1,0,0.8,1&…`

**Crop 20% off the bottom edge of an image:**

`…&cropN=0,0,1,0.8&…`

## See also {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
