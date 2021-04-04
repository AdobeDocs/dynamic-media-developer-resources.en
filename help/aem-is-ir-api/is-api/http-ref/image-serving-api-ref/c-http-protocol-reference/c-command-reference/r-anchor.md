---
description: Image Anchor. Defines the anchor point of the image, solid color, or text bounding box rectangle, before applying transforms (crop=, scale=, rotate=, flip=). Also serves as the center-of-rotation for rotate=.
solution: Experience Manager
title: anchor
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
---
# anchor{#anchor}

Image Anchor. Defines the anchor point of the image, solid color, or text bounding box rectangle, before applying transforms (crop=, scale=, rotate=, flip=). Also serves as the center-of-rotation for rotate=.

 `anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p>pixel offset from the top-left corner of the source image (int, int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>normalized offset from the center of the source image (real, real) </p></td> 
 </tr> 
</table>

The anchor point is transformed with the image and becomes the layer origin point (unless `origin=` is specified as well, in which case `anchor=` is used only as the center-of-rotation for `rotate=`).

`anchorN=0,0` places the image anchor at the center of the source image. `anchorN=-0.5,-0.5` or `anchor=0,0` is at the top-left corner, and `anchorN=0.5,0.5` is at the bottom-right corner of the source image.

## Properties {#section-f08942bc6aae46a8b5d341faaff80640}

Source image attribute. Applies to the current layer or to layer 0 if `layer=comp`.

## Default {#section-35d369fab1254f1a9b91684a6e169ad1}

If `anchor=` is not specified, catalog::Anchor is used. If `catalog::Anchor` is not defined, the center of the image rectangle is used (same as specifying `anchorN=0,0`).

Text layers involving `textPs=` and layers involving `clipPath=` may have different default anchors.

## Example {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

See "Example C" in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## See also {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog::Anchor](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
