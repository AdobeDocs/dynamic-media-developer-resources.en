---
title: rotate
description: Rotate image. Rotates the image, text, or solid color layer by the specified angle.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
TQID: 'https://experienceleague.adobe.com/WDC8SRJEBqspJidlNPxLvwmX-HMQG1zC6wwHNJIXLK4'
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
# rotate{#rotate}

Rotate image. Rotates the image, text, or solid color layer by the specified angle.

 `rotate= *`angle`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> angle</span> </p> </td> 
  <td class="stentry"> <p>Rotation angle in degrees (real). </p></td> 
 </tr> 
</table>

Positive angles rotate clockwise. The layer anchor point ( `anchor=` or `catalog::Anchor`) serves as the center-of-rotation. The layer rectangle is enlarged and fitted around the rotated data as needed to avoid cropping. Rotation is applied after filling the layer's background area with `color=`. The modifier `bgColor=` can be used to add background color to the bounding rectangle after rotation.

## Properties {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Layer command. Applies to the current layer or to layer 0 if `layer=comp`. Ignored by effect layers.

## Default {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, for no rotation.

## Example {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Place an "On Sale" label near the top-left corner of images in an image catalog. The label image is already sized correctly for the 300x300 view and should be rotated 30° to the left. To enhance the label, fill the text box with a white, semi-opaque color.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Apply `size=` to layer 0 to set the view size, rather than using `wid=` and `hei=`. This method allows `myImageId` to be resized while not changing the final size of `labelImage`. Also, specify `scl=1`, otherwise the composite image might be scaled to `attribute::DefaultPix` (unless that is set to 0,0). The modifier `color=` adds the semi-opaque background color to the text box before rotation.

The origin for both layers is set to the top-left corner to achieve the desired alignment. The origin point for layer 1 applies to `labelImage`after it is rotated.

See [Example A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) for an example of rotated text.

## See also {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
