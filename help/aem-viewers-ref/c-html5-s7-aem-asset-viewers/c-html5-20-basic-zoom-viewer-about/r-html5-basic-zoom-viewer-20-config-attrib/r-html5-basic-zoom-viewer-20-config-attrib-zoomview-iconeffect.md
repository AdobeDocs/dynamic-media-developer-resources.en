---
description: null
seo-description: null
seo-title: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
topic: Dynamic media
uuid: 38350e3d-515b-454c-bc85-39b91ad06e8b
index: y
internal: n
snippet: y
---

# ZoomView.iconeffect{#zoomview-iconeffect}

 ` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Enables the IconEffect to display on the top of the image when the image is in a reset state and it is suggestive of an available action to interact with the image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies the maximum number of times the IconEffect appears and reappears. A value of <span class="codeph"> -1</span> indicates that the icon always reappears indefinitely. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifies the duration of the show or hide animation, in seconds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p>Sets the number of seconds that the IconEffect stays fully visible before it auto hides. That is, the time after the fade-in animation is completed but before the fade out animation starts. A setting of <span class="codeph"> 0</span> disables the auto-hide behavior. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Default {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## Example {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0` 
