---
description: Configuration attribute for Video Viewer.
seo-description: Configuration attribute for Video Viewer.
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 1ba6f24a-77bb-41ef-a831-a7ac817abd73
index: y
internal: n
snippet: y
---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Configuration attribute for Video Viewer.

 ` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
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

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```

