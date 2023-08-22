---
title: op_contrast
description: Adjust contrast. Adjusts the image contrast by increasing the brightness of pixels with more than 50% brightness, and reducing the brightness of pixels with less than 50% brightness.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
---
# op_contrast{#op-contrast}

Adjust contrast. Adjusts the image contrast by increasing the brightness of pixels with more than 50% brightness, and reducing the brightness of pixels with less than 50% brightness.

 `op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Contrast adjustment in percent (-100…100 int). </p></td> 
 </tr> 
</table>

## Properties {#section-d319ed55057344eab0a3c93f720acdbf}

Layer command. Applies to the current layer or to the composite image if `layer=comp`. Ignored by effect layers.

## Default {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, for no change in contrast. CMYK images or layers are converted to RGB before the operation is applied.

## Example {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Decrease the contrast and sharpness of a higher quality image layer to visually match it to a low-quality background photo:

… `&op_blur=3&op_contrast=-12&`

A future release may use the median brightness of the image rather than a fixed 50% brightness.
