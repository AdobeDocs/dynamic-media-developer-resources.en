---
description: null
seo-description: null
seo-title: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic media
uuid: 42327f03-269b-4d4e-a35d-2537ca3ba071
index: y
internal: n
snippet: y
---

# ZoomView.singleclick{#zoomview-singleclick}

 `[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configures the mapping of single-click/tap to zoom actions. Setting to <span class="codeph"> none </span> disables single-click/tap zoom. If set to <span class="codeph"> zoom </span> clicking the image zooms in one zoom step; CTRL+Click zooms out one zoom step. Setting to <span class="codeph"> reset </span> causes a single click on the image to reset the zoom to the initial zoom level. For <span class="codeph"> zoomReset </span>, reset is applied if the current zoom factor is at or beyond the specified limit, otherwise zoom is applied. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Default {#section-7564169749ff4a4996049ea1148cb2a5}

`zoomReset` on desktop computers; `none` on touch devices.

## Example {#section-96e69b70365f461dae4399e49044ea2f}

`singleclick=zoom` 
