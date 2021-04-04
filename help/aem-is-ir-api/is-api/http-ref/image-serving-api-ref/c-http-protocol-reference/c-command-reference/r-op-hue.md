---
description: Adjust hue. Shifts the hue of each visible pixel of the layer or composite image by the specified amount.
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
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
