---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
---
# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

 ` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Configures how the component fetches new images for the main and flyout view during resize. </p> <p>When set to <span class="codeph"> 0 </span>, the component does not load new images during resize; image resolution in the flyout view does not change. </p> <p>Setting to <span class="codeph"> 1 </span> lets you specify one or more width breakpoints for the image loaded into the main view. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breakpoint, <span class="varname"> width </span>[; <span class="varname"> width </span>] </span> </p> </td> 
   <td colname="col2"> <p> Width breakpoints for the image that is loaded into the main view. The component always uses the best fit size for the initial load. After resize, it ensures that the image in the main view is always downloaded with the width equal to closest larger breakpoint, and downscaled on the client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
