---
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
---
# ControlBar.transition{#controlbar-transition}

Configuration attribute for Interactive Video Viewer.

 ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Specifies the effect type which will be used to show/hide the control bar and its content. </p> <p>Set to <span class="codeph"> none</span> for instant show/hide. </p> <p>Set to <span class="codeph"> fade</span> to provide a gradual fade in/out effect. Not supported on Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the time in seconds between the last mouse/touch event registered by the control bar and the time control bar hides. If set to <span class="codeph"> -1</span> the component never triggers its auto-hide effect and, therefore, always stays visible on the screen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> Sets the duration of the fade in/out animation, in seconds. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
