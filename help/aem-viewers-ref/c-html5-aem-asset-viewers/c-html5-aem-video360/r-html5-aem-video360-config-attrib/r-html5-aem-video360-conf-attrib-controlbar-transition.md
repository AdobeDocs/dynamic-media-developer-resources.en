---
description: Configuration attribute for Video360 Viewer.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: 950b1230-5c4b-4222-87e2-d069287fc3ff
---
# ControlBar.transition{#controlbar-transition}

Configuration attribute for Video360 Viewer.

 ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Specifies the effect type that is used to show or hide the control bar and its content. </p> <p>Use <span class="codeph"> none</span> for instant show and hide. Use <span class="codeph"> fade</span> to provide a gradual fade in and fade out effect. </p> <p>Fade is not supported on Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifies the time in seconds between the last mouse/touch event that the control bar registers and the time control bar hides. </p> <p> If set to <span class="codeph"> -1</span> the component never triggers its auto-hide effect and always stays visible on the screen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>Sets the duration of the fade in and fade out animation, in seconds. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
