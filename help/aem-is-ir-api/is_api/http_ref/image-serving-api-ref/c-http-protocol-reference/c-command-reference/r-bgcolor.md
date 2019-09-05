---
description: Layer Background Color. Specifies the background color and opacity of the current layer.
seo-description: Layer Background Color. Specifies the background color and opacity of the current layer.
seo-title: bgColor
solution: Experience Manager
title: bgColor
topic: Scene7 Image Serving - Image Rendering API
uuid: f66aa5a3-ae01-4f90-bda9-cb237378ba30
index: y
internal: n
snippet: y
---

# bgColor{#bgcolor}

Layer Background Color. Specifies the background color and opacity of the current layer.

 `bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span></span> </p> </td> 
  <td class="stentry"> <p>Gray, RGB, or CMYK color value, with or without alpha. </p></td> 
 </tr> 
</table>

Transparent and semi-opaque areas within the bounding rectangle of the layer are filled with the specified color* after* `opac=`, `rotate=`, and `extend=` are applied.

## Properties {#section-19dfc13e997f4a33889a1df1e4ad50b9}

Layer attribute. Applies to current layer or to layer 0 if `layer=comp`. Ignored by effect layers.

*`color`* is assumed to exist in the working color space corresponding to the pixel type of *`color`*. *`color`* is converted accurately if the final layer image has a different pixel type.

## Default {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0 (fully transparent).

## Example {#section-6e14fcf1d31e432dbdb56b9320904453}

See [color=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423).

## See also {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [color=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423), [blendMode=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172), [opac=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extend=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [rotate=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [bgc=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Color Management](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7) 
