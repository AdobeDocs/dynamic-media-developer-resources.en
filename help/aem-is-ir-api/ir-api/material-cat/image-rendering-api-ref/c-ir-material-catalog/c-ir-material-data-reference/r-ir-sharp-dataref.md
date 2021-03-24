---
description: Sharpening. Sharpening attribute, determines when the material is sharpened during rendering.
solution: Experience Manager
title: Sharp
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Sharp{#sharp}

Sharpening. Sharpening attribute, determines when the material is sharpened during rendering.

The type and amount of sharpening is controlled by the vignette via a default material template or with `catalog::RenderSettings`.

## Properties {#section-aac81b1a611b4bca90b8544eae7896df}

Enum.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>No sharpening. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Normal sharpening (after the transform). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Alternate sharpening (before the transform). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>More sharpening (both before and after the transform). </p></td> 
 </tr> 
</table>

Ignored by solid color materials, optional for all other materials.

## Default {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` is used if the field is not present, if it is empty, or if the value is not one of the supported choices.

## See also {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribute::Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a) 
