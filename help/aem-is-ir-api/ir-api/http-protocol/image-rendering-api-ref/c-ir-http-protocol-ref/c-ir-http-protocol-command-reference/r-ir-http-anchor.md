---
description: Image anchor (hotspot). Specifies the texture anchor point (hotspot) of the repeatable texture or decal material.
seo-description: Image anchor (hotspot). Specifies the texture anchor point (hotspot) of the repeatable texture or decal material.
seo-title: anchor
solution: Experience Manager
title: anchor
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
---

# anchor{#anchor}

Image anchor (hotspot). Specifies the texture anchor point (hotspot) of the repeatable texture or decal material.

 `anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Pixel offset from the top-left corner of the source image (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Normalized offset from the center of the source image (real, real). </p></td> 
 </tr> 
</table>

A repeatable texture is applied to a vignette object, so that the texture anchor point ( `anchor=`) is located at the object's texture origin point.

A decal image is applied to a vignette object, so that the decal anchor point is located at the object's decal origin point. The decal position can be further adjusted using the `pos=` command.

`anchorN=0,0` places the image anchor at the center of the source image. `anchorN=-0.5,-0.5` or `anchor=0,0` is at the top-left corner, and `anchorN=0.5,0.5` is at the bottom-right corner of the source image.

## Properties {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Material attribute**. Ignored if `align=2`, or if the material is not a repeatable texture, a wallpaper, nor a decal.

## Default {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, if the material is based on a catalog entry. Otherwise, `anchor=0,0` (the top-left corner of the image) for repeatable textures and wallpapers, and `anchorN=0,0` (the center of the image) for decals.

## See also {#section-b18bf0b035644ca5aedebbc64373718e}

[catalog::Anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7) 
