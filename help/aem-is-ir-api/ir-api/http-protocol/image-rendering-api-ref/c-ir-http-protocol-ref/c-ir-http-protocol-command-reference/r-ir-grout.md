---
description: Tile grout color and thickness. Simulates grout for ceramic and natural stone tiles.
solution: Experience Manager
title: grout
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
---
# grout{#grout}

Tile grout color and thickness. Simulates grout for ceramic and natural stone tiles.

grout= *`color`*[, *`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color </span> </span> </p> </td> 
  <td class="stentry"> <p>Grout color (gray or RGB). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>Grout thickness; scene coordinate units (typically inches) (real). </p> </td> 
 </tr> 
</table>

For maximum control of the grout appearance the following requirements apply:

* The tile must be square or rectangular; no other shapes are supported at this time. 
* The image must contain a single tile only. 
* The default grout in the image (if any) must have exactly the same thickness on all four edges. 
* The thickness of the default grout must be specified in the material catalog ( `catalog::GroutWidth`).

## Properties {#section-de78b678245b4ffda48097c345949e77}

Material attribute. `*`color`*` must be an RGB color value. `*`width`*` must be a real value 0 or larger.

Ignored if repeat = 4, 5, 7, 8, 9, 14, or higher, or when specified for materials other than repeatable textures.

## Default {#section-bfab3621f70b4489a21994ab11b20cc6}

If `grout=` is not specified, the grout in the image is not modified. If ` grout= *`color`*` is specified, `*`width`*` defaults to `catalog::GroutWidth`.

## See also {#section-8d472906a44943f5a8557e98f2fbc71f}

[Color Values](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
