---
description: null
seo-description: null
seo-title: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
topic: Dynamic media
uuid: 31575fa3-8cc4-468e-b590-77edc3b148d4
---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

 [!DNL `[ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`]

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Enables or disables the ability for a user to scroll the swatches with a mouse or by using touch gestures </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Functions within the <span class="codeph"> 0-1 </span> range. It is a <span class="codeph"> % </span> value for movement in the wrong direction of the actual speed. If it is set to <span class="codeph"> 1 </span>, it moves with the mouse. If it is set to <span class="codeph"> 0 </span>, it does not let you move in the wrong direction at all. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-831c23dea82449bfa50fd155bea365b7}

Optional.

## Default {#section-464be2db89f34516ad93f32f7783d2b0}

[!DNL `1,0.5`]

## Example {#section-e67c8807762e471bb03d6a8fb20e19d4}

[!DNL `enabledragging=0`] 
