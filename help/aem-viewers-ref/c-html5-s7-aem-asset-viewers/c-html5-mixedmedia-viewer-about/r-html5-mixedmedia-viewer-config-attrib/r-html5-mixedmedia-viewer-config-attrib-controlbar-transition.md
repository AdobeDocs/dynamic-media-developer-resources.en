---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition

feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
---
# ControlBar.transition{#controlbar-transition}

 ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
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

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
