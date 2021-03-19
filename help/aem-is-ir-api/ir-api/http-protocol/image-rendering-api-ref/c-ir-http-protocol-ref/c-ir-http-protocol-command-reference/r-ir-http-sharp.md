---
description: Sharpen texture. Specifies the sharpening to be applied when rendering this material.
seo-description: Sharpen texture. Specifies the sharpening to be applied when rendering this material.
seo-title: sharp
solution: Experience Manager
title: sharp
uuid: 8265eebf-9cec-4ad3-8b22-0f46f33a89f1
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# sharp{#sharp}

Sharpen texture. Specifies the sharpening to be applied when rendering this material.

 `sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>No sharpening. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Normal sharpening (late). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 alternate sharpening (early). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>More sharpening (early and late). </p> </td> 
 </tr> 
</table>

`sharp=1` applies sharpening after the material is rendered; `sharp=2` applies sharpening after initial scaling of the texture, but before it is transformed into the scene; `sharp=3` applies sharpening both before and after the transform.

The sharpening algorithm and amount of sharpening and other USM (unsharp masking) parameters are controlled by the default material template provided by the vignette or with `rs=`.

## Properties {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Material attribute. Ignored by solid color materials.

## Default {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, if the material is based on a catalog entry, otherwise `attribute::Sharp`.

## See also {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf) 
