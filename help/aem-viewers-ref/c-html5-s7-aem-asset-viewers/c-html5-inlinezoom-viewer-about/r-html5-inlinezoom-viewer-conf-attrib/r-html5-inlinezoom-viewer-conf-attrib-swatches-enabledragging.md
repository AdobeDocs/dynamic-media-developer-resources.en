---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 9b69f6d7-b7a1-42c6-98d7-80952b7f8b31
---
# Swatches.enabledragging{#swatches-enabledragging}

 ` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

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

## Properties {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Default {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,0.5`

## Example {#section-3a188ab955c445bcb2efa3c49722c10d}

`enabledragging=0`
