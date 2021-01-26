---
description: Configures how the component fetches new images for the main and flyout view during resize.
seo-description: Configures how the component fetches new images for the main and flyout view during resize.
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic Media
uuid: 5cded4cb-7b02-47da-9e2d-b236548cc61d
---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configures how the component fetches new images for the main and flyout view during resize.

 ` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p>When set to <span class="codeph"> 0 </span>, the component does not load new images during resize, and image resolution in the flyout view does not change. </p> <p>When set to <span class="codeph"> 1 </span> lets you specify one or more width breakpoints for the image loaded into the main view. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> breakpoint, <span class="varname"> width </span>[; <span class="varname"> width </span>] </span> </p> </td> 
   <td colname="col2"> <p>Width breakpoints for the image loaded into main view. The component will always use best fit size for the initial load. After resize it will ensure that the image in main view is always downloaded with the width equal to closest bigger breakpoint, and downscaled on the client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600` 
