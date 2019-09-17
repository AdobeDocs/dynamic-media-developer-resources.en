---
description: null
seo-description: null
seo-title: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
topic: Dynamic media
uuid: ad423dc7-4dd8-42d9-bf75-db8f309f6aaa
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

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0` 
