---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
uuid: 8c4e6bf8-0238-470b-9fbe-262eb17f8f3b
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

 ` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies the image magnification for the flyout view, relative to the main view. Must be an integer or floating point value <span class="codeph"> 1.0</span> or larger. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> An optional secondary factor can be specified which is accessible by clicking or tapping on the main view when the highlight is active. Clicking or tapping a second time reverts to the primary zoom factor. A value of <span class="codeph"> -1</span> disables the secondary zoom factor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Specifies how the component handles small images. </p> <p>If set to <span class="codeph"> 1</span> the component upscales the main image so that it fits within the main view. Also, it upscales the zoom image so that it completely fills the configured flyout window area. </p> <p>If set to <span class="codeph"> 0</span> small images are displayed at their original resolution and display centered in the main view area and inside the flyout window. You can configure extra white space around the image with a background or similar CSS property of the <span class="codeph"> s7flyoutzoomview</span> and <span class="codeph"> s7flyoutzoom</span> CSS classes in the main view and flyout window, respectively. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Default {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Example {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0` 
