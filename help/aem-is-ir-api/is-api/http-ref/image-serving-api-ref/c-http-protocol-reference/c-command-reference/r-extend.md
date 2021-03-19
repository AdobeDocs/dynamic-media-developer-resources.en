---
description: Extend layer. Adds margins to a layer or crops the layer rectangle.
seo-description: Extend layer. Adds margins to a layer or crops the layer rectangle.
seo-title: extend
solution: Experience Manager
title: extend
uuid: 7ca69994-e788-41a9-93ac-f22b6b9920d0
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# extend{#extend}

Extend layer. Adds margins to a layer or crops the layer rectangle.

 `extend= *`left`*, *`top`*, *`right`*, *`bottom`*`

`extendN= *`leftN`*, *`topN`*, *`rightN`*, *`bottomN`*`

<table id="simpletable_1DCCD469712B423C8154630127DC5F54"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> left,top,bottom,right</span></span> </p></td> 
  <td class="stentry"> <p>Number of pixels to add to (or remove from, if the value is negative) the left, top, right, and bottom edge of the layer rect (int, int, int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> leftN,topN,bottomN,rightN</span></span> </p></td> 
  <td class="stentry"> <p>Amount of space to add to (or remove from, if the value is negative) the left, top, right, and bottom edge of the layer rect, expressed as normalized amounts relative to the size of the original layer rect (real, real, real, real). </p></td> 
 </tr> 
</table>

`extend=` is applied to the layer *after* the image is cropped ( `crop=`) and all layer transforms, including `rotate=`, have been applied.

The extended area is filled with `bgColor=`, or, if not specified, remains transparent.

Argument values for `extendN=` are normalized relative to the size of the layer rect after layer transforms, including `rotate=` have been applied.

## Properties {#section-8fc94de871f841f3bf5e1df135972ca9}

Layer attribute. Applies to layer 0 if `layer=comp`. Ignored by effect layers.

## Default {#section-de7473649cb9406b8d99028c74c4b8dc}

`extend=0,0,0,0`, for no change of the layer rectangle.

## Examples {#section-cc6d8e76f3dd4607ac31cb095d86c9fe}

**Crop an image and then add a 5 pixel wide, red border:**

`…&cropN=.2,.3,.8,.9&extend=5,5,5,5&bgColor=255,0,0&…`

**Scale an image to 200 pixels width and add title text into a 30 pixel margin above the image.**

Note that the height of the composite image varies depending on the aspect ratio of the image.

`http://server/myRootId/myImageId?size=200,0&extend=0,30,0,0&origin=0,0 layer=1&text=title-text&origin=0,0`

## See also {#section-2d9572be32ca4602b60920b3810f3638}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b), [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) 
