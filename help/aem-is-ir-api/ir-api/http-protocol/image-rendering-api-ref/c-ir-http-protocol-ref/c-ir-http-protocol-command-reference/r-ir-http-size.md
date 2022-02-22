---
title: size
description: Decal size. Specifies the size of a decal material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
---
# size{#size}

Decal size. Specifies the size of a decal material.

 ` size= *`width,height`*[ *`,thickness`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> width, height </span> </p> </td> 
  <td class="stentry"> <p>Size of the decal object in scene coordinate units (typically inches) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> thickness </span> </p> </td> 
  <td class="stentry"> <p>Thickness of the decal object in scene coordinate units (typically inches) (real). </p> </td> 
 </tr> 
</table>

If neither width or height is 0, the image is scaled to the exact specified dimensions and the aspect ratio of the image is not preserved. Setting either value to 0 preserves the aspect ratio of the image.

If *`thickness`* is specified, a drop shadow is rendered if the vignette object defines an appropriate light vector. Set *`thickness`* to 0 to disable drop-shadow rendering.

## Properties {#section-818e01e91fed4015951189c818ef28d8}

Material attribute. Only used by decals; ignored by all other materials. `res=` is ignored if either width or height is greater than 0. Values must not be negative.

## Default {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` if the decal material is based on a catalog entry; otherwise `size=0,0,0`. The decal size is calculated from `res=` if *`wid`* and *`hei`* are not specified or are set to 0. No drop shadow is rendered if *`thickness`* is not specified or set to 0.

## Example {#section-04fdc2b60b9e4071b672bf6a913738ad}

A MSS for a decal, which is sized based on resolution, rotated by 20 deg clockwise, and has a thickness of 2.5 inches, for an appropriate drop shadow effect:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## See also {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Scene Coordinates](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
