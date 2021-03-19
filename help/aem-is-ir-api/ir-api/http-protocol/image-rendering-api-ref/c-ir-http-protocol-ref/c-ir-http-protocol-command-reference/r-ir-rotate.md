---
description: Material rotation angle. Defines the rotation angle for materials.
seo-description: Material rotation angle. Defines the rotation angle for materials.
seo-title: rotate
solution: Experience Manager
title: rotate
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# rotate{#rotate}

Material rotation angle. Defines the rotation angle for materials.

 ` rotate= *`angle`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> angle </span> </p> </td> 
  <td class="stentry"> <p>Rotation angle in degrees (real). </p> </td> 
 </tr> 
</table>

Rotate repeatable texture materials (excluding wallpapers) by multiples of 45 degrees when applied to Flat Objects or Plane Objects.

Rotate repeatable texture materials by arbitrary angles when applied to Flowline and Sketch Objects.

Rotate decal materials by arbitrary angles.

Positive angles rotate clockwise. The texture or decal is rotated around the anchor point ( `anchor=`); the anchor point remains aligned with the target object's origin.

## Properties {#section-ad4d07897ca24f63af1a4062f8618e36}

Material attribute. Ignored by solid color, wallpaper, cabinet, and window treatment materials. *`angle`* must be a multiple of 45 for repeatable textures, unless applied to Flowline or Sketch Objects.

## Default {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, for no rotation.

## See also {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26) 
