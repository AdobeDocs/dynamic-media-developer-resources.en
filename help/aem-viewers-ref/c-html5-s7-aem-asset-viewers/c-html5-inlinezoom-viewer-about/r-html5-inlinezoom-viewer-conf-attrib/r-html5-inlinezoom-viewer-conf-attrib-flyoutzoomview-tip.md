---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip

feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
---
# FlyoutZoomView.tip{#flyoutzoomview-tip}

 ` [FlyoutZoomView.|<containerId>_flyout.]tip= *`duration`*[, *`count`*][, *`fade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifies the number of seconds the tip text is displayed before it hides. When set to <span class="codeph"> -1</span>, the message is always displayed, even if the user activates the flyout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifies the number of times the text is displayed when viewing new images in the set. A value of <span class="codeph"> -1</span> means that the text is always displayed when viewing any image in the set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifies the duration of a fade animation that occurs when the text appears or disappears. A value of <span class="codeph"> 0</span> means no fade transition. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Default {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## Example {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
