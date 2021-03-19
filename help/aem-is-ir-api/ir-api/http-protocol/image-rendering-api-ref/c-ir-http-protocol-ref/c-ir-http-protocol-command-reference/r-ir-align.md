---
description: Texture render alignment. Specifies which of the origin points defined by the selected vignette object is to be used.
seo-description: Texture render alignment. Specifies which of the origin points defined by the selected vignette object is to be used.
seo-title: align
solution: Experience Manager
title: align
uuid: 0b24cd82-f9b2-48f4-9052-8c2026370ff7
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# align{#align}

Texture render alignment. Specifies which of the origin points defined by the selected vignette object is to be used.

 `align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Default (center-match) origin. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Continuous match origin. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Random alignment. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>User-defined origin. </p></td> 
 </tr> 
</table>

The renderer applies the texture to the object so that the texture anchor point ( `anchor=`) coincides with the specified origin point.

Each object can define up to 6 origin points (0,1, 3, 4, 5, 6). If an `align` value is specified but the corresponding origin point is not defined by the vignette object, the default (center-match) origin point is used.

`align=2` specifies random texture alignment, in which case `anchor=` is effectively ignored.

Mostly used for upholstery materials, possibly for apparel fabrics, to manage the alignment of the texture between adjacent objects.

## Properties {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Material attribute. Ignored if a wall, cabinet, appliance, or window coverings frame object is selected, or if the material is not a repeatable texture.

## Default {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, if the material is based on a catalog entry, otherwise 0 (center-matched).

## See also {#section-945d1ce275df487d9d564d4043156c79}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26) 
