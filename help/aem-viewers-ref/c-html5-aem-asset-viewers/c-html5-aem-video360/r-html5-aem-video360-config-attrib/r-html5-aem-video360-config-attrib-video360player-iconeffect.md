---
description: Configuration attribute for Video360 Viewer.
seo-description: Configuration attribute for Video360 Viewer.
seo-title: Video360Player.iconeffect
solution: Experience Manager
title: Video360Player.iconeffect
uuid: a0a2f840-e330-4636-8daf-1cd3f2eddf01
feature: "Dynamic Media Classic,Viewers,SDK/API,360 VR Video"
role: "Developer,Business Practitioner"
---

# Video360Player.iconeffect{#video-player-iconeffect}

Configuration attribute for Video360 Viewer.

 ` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Enables the IconEffect to be displayed on top of the video when the video is in a paused state. On some devices native controls are used. In such cases, the <span class="codeph"> iconeffect</span> modifier is ignored. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the maximum number of times the IconEffect appears and reappears. A value of <span class="codeph"> -1</span> indicates that the icon reappears indefinitely. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the duration of show or hide animation, in seconds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Sets the number of seconds that the IconEffect stays fully visible before it auto-hides. That is, the time after the fade in animation is completed and before the fade out animation starts. Set to <span class="codeph"> 0</span> to disable auto-hide behavior. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0` 
