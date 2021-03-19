---
description: Adjust hue. Shifts the hue of each visible pixel of the layer or composite image by the specified amount.
seo-description: Adjust hue. Shifts the hue of each visible pixel of the layer or composite image by the specified amount.
seo-title: op_hue
solution: Experience Manager
title: op_hue
uuid: 23da539e-0192-4dc4-a19b-41aa94a82730
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# op_hue{#op-hue}

Adjust hue. Shifts the hue of each visible pixel of the layer or composite image by the specified amount.

 `op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Hue adjustment in degrees (-180…+180 int). </p></td> 
 </tr> 
</table>

Based on a 360 degree hue range.

## Properties {#section-55779644700b4c808a624cdf5a04447e}

Layer command. Applies to the current layer or to the composite image if `layer=comp`. Ignored by effect layers. CMYK images or layers are converted to RGB before the operation is applied.

## Default {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, for no change in hue. 
