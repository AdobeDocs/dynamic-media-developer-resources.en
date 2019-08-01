---
description: null
seo-description: null
seo-title: SpinView.iconeffect
solution: Experience Manager
title: SpinView.iconeffect
topic: Dynamic media
uuid: f568a98d-1b34-4a85-bd2f-e67a34b3a3e9
index: y
internal: n
snippet: y
---

# SpinView.iconeffect{#spinview-iconeffect}

 ` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_DF2137DF9C7441B381D2B03CEE4B880A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Enables the <span class="codeph"> iconeffect</span> to display on the top of the image when the image is in a reset state and it is suggestive of an available action to interact with the image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the maximum number of times the <span class="codeph"> iconeffect</span> appears and reappears. A value of <span class="codeph"> -1</span> indicates that the icon always reappears indefinitely. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p>Specifies the duration of the show or hide animation, in seconds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Sets the number of seconds that the <span class="codeph"> iconeffect</span> stays fully visible before it auto hides. That is, the time after the fade-in animation is completed but before the fade out animation starts. A setting of <span class="codeph"> 0</span> disables the auto-hide behavior. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0` 
