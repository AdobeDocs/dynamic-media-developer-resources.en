---
title: op_blur
description: Blur image. Applies a blur filter to the image data.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
---
# op_blur{#op-blur}

Blur image. Applies a blur filter to the image data.

 `op_blur= *`radius`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Blur filter radius in pixels (real 0..100). </p></td> 
 </tr> 
</table>

*`radius`* is in pixels relative to the composite image. Also used to feather layer effects.

## Properties {#section-92573fe2c07746a7bab93a81fc3d208d}

Layer command. Applies to the current layer or to the composite image if `layer=comp`.

## Default {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, for no blur effect.

## Example {#section-1ebacde68388492eb108ae0fcd7424db}

Blur the background of an image. A separate mask image is referenced by `catalog::MaskPath`. Note that `layer=0`must be specified explicitly, otherwise `op_blur` would be applied to the entire composite image.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
