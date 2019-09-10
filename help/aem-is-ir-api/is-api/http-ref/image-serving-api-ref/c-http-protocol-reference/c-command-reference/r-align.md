---
description: Align Image with View. Aligns the composite image (possibly after scaling, if scl= is specified as well) within the view rectangle defined by wid= and hei=.
seo-description: Align Image with View. Aligns the composite image (possibly after scaling, if scl= is specified as well) within the view rectangle defined by wid= and hei=.
seo-title: align
solution: Experience Manager
title: align
topic: Scene7 Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
index: y
internal: n
snippet: y
---

# align{#align}

Align Image with View. Aligns the composite image (possibly after scaling, if scl= is specified as well) within the view rectangle defined by wid= and hei=.

 ` align= *`horiz`*, *`vert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span> </span> </p> </td> 
  <td class="stentry"> <p>horizontal alignment (real, -1.0…1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span> </span> </p> </td> 
  <td class="stentry"> <p>vertical alignment (real, -1.0…1.0) </p> </td> 
 </tr> 
</table>

Specify `align=-1,-1` to align the top-left of the composite image with the top-left of the view, specify `align=1,1` to align the bottom, right of the image with the bottom right of the view. For standard image and thumbnail requests, any area of the view which is not covered by composite image data is filled with `bgc=`.

## Properties {#section-3fbec8206fc944eda4746d8be84f3b41}

View attribute. ( `align=` is also used to define the alignment between a watermark image and the composite image to which the watermark is applied.) Applies regardless of current layer setting. Ignored if only one of `wid=` and `hei=` is specified and when `fit=constrain` or `fit=stretch`.

## Default {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, which centers the image in the view rectangle.

## Example {#section-2c9447aa2e184fb8ab1a4370dc61d554}

The following request fits `myImage` into a 200x200 pixel view rectangle.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

If `myImage` is exactly square, it fills the entire view rectangle. If `myImage` has a portrait aspect ratio, it is scaled to be 200 pixels tall and is centered horizontally in the view. If `myImage` has a landscape aspect ratio, it is scaled to be 200 pixels wide and is aligned to the top edge of the view. In all cases, the image returned is exactly 200x200 pixels in size; any space not covered by the scaled `myImage` is filled with `attribute::BkgColor` (specify bgc= to control the background color dynamically).

## See also {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Watermarks](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832) 
