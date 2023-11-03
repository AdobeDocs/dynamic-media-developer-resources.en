---
title: ControlBar.transition
description: Specifies the effect type that is used to show or hide the control bar and its content.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
---
# ControlBar.transition{#controlbar-transition}

 ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade </span> </p> </td> 
   <td colname="col2"> <p> Specifies the effect type that is used to show or hide the control bar and its content. Use <span class="codeph"> none </span> for instant show and hide; <span class="codeph"> fade </span> provides a gradual fade in and fade-out effect (not supported on Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies the time in seconds between the last mouse/touch event that the control bar registers and the hiding of the time control bar. </p> <p> If set to <span class="codeph"> -1 </span>, the component never triggers its auto-hide effect and always stay visible on the screen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration </span> </span> </p> </td> 
   <td colname="col2"> <p> Sets the duration of the fade in and fade-out animation, in seconds. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional. This command is ignored on touch devices, where the control bar auto-hide is disabled.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
