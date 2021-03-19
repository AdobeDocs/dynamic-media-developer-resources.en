---
description: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
uuid: 98a84ba1-4b89-424a-ac2e-4a59af33cec0
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

 ` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Configures how the component fetches new images for the main and flyout view during resize. </p> <p>Set to <span class="codeph"> 0 </span>, the component does not load new images during resize, and image resolution in the flyout view does not change. </p> <p>Set to <span class="codeph"> 1 </span> lets you specify one or more width breakpoints for the image loaded into the main view. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breakpoint, <span class="varname"> width </span>; <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p>Width breakpoints for the image that is loaded into the main view. </p> <p>The component always uses the best fit size for the initial load. After resize it ensures that the image in the main view is always downloaded using the width that is equal to the closest larger breakpoint, and downscaled on the client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Default {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Example {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600` 
