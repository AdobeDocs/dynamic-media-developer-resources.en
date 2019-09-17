---
description: null
seo-description: null
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 8e112f3c-8fa6-4c77-94c5-5027275225e7
---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

 ` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Enables the IconEffect to display on top of the video when the video is paused. On some devices native controls are used. In such case, the <span class="codeph"> iconeffect</span> modifier is ignored. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies the maximum number of times the IconEffect appears and reappears. A value of <span class="codeph"> -1</span> indicates that the icon reappears indefinitely. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies the duration of show or hide animation, in seconds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Sets number of seconds that the IconEffect stays visible before it auto-hides. That is, the time after fade-in animation is completed and before fade-out animation starts. A setting of <span class="codeph"> 0</span> disables auto-hide behavior. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0` 
