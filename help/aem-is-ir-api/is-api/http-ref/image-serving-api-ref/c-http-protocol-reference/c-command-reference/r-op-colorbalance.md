---
description: Adjust color balance. Adjusts the value of each RGB color component separately.
seo-description: Adjust color balance. Adjusts the value of each RGB color component separately.
seo-title: op_colorbalance
solution: Experience Manager
title: op_colorbalance
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
---

# op_colorbalance{#op-colorbalance}

Adjust color balance. Adjusts the value of each RGB color component separately.

 `op_colorbalance= *`redAdj`*, *`greenAdj`*, *`blueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Red component adjustment (-100…+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Green component adjustment (-100…+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Blue component adjustment (-100…+100 int). </p></td> 
 </tr> 
</table>

Gray and CMYK input image data is converted to RGB using naive conversion which is not accurate when color management is enabled.

## Properties {#section-dff9c934f7c1442bbd02379b688d82e2}

Layer command. Applies to the current layer or to the composite image if `layer=comp`. Ignored by effect layers. CMYK images and layers are converted to RGB before the operation is applied.

## Default {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` for no change in colors.

## Example {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Push the color balance towards red:

… `&op_colorBalance=100,0,0&`… 
