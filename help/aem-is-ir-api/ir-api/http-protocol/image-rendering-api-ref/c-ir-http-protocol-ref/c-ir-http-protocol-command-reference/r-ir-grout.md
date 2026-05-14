---
title: grout
description: Tile grout color and thickness. Simulates grout for ceramic and natural stone tiles.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
TQID: 'https://experienceleague.adobe.com/FrYxcizVu3nXej1tt4QpX0AsLEylXTfwYRaSQP43HNI'
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
# grout {#grout}

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

For maximum control of the grout appearance, the following requirements apply:

* The tile must be square or rectangular; no other shapes are currently supported.
* The image must contain a single tile only.
* The default grout in the image (if any) must have the same thickness on all four edges.
* The thickness of the default grout must be specified in the material catalog ( `catalog::GroutWidth`).

## Properties {#section-de78b678245b4ffda48097c345949e77}

Material attribute. `*`color`*` Must be an RGB color value. `*`width`*` must be a real value 0 or larger.

Ignored if repeat = 4, 5, 7, 8, 9, 14, or higher, or when specified for materials other than repeatable textures.

## Default {#section-bfab3621f70b4489a21994ab11b20cc6}

If `grout=` is not specified, the grout in the image is not modified. If `grout= *`color`*` is specified, `*`width`*` defaults to `catalog::GroutWidth`.

## See also {#section-8d472906a44943f5a8557e98f2fbc71f}

[Color Values](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
