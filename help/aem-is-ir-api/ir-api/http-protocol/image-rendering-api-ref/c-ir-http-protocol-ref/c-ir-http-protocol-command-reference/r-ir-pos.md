---
title: pos
description: Decal position. Defines the offset in inches from the anchor= point of the decal image to the decal origin point defined by the target vignette object.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 531f1465-2bec-46b6-a41e-54d993cbf410
---
# pos{#pos}

Decal position. Defines the offset in inches from the anchor= point of the decal image to the decal origin point defined by the target vignette object.

 `pos=x,y`

<table id="simpletable_DB3B64EFB67A47AD843812324ABFAE45"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,<span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Relative position adjustment in scene coordinate units (typically inches) (real, real). </p></td> 
 </tr> 
</table>

## Properties {#section-50371cfa4e244bc49d2295a918749258}

Material attribute. Ignored by materials other than decals.

## Default {#section-1b66efab054c45ca8d67d6a9865020f4}

`pos=0,0`. Aligns the decal's anchor point with the vignette object's decal origin.

## See also {#section-7cd8139481334ed79704d628b5bbd236}

[Scene Coordinates](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
