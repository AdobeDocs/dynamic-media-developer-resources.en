---
title: CallToAction.enabledragging
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 21db58df-b76e-4a78-afc4-5e0188cb8896
---
# CallToAction.enabledragging{#calltoaction-enabledragging}

Configuration attribute for Interactive Video Viewer.

 ` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Enables or disables the ability for a user to scroll the thumbnails with a mouse or by using touch gestures. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td colname="col2"> <p> Is in the <span class="codeph"> 0-1 </span> range and it is a percent value for the movement in the wrong direction of the actual speed. </p> <p>If set to <span class="codeph"> 1 </span>, it moves with the mouse. </p> <p>If set to <span class="codeph"> 0 </span>, it does not let you move in the wrong direction. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```
