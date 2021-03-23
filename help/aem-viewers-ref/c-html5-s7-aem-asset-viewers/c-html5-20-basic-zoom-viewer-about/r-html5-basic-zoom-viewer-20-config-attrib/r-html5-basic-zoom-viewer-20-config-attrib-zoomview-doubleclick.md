---
description: ZoomView.doubleclick
solution: Experience Manager
title: ZoomView.doubleclick

feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
---

# ZoomView.doubleclick{#zoomview-doubleclick}

 `[ZoomView.|<containerId>_zoomView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configures the mapping of double-click/tap to zoom actions. Setting to <span class="codeph"> none </span> disables double-click/tap zoom. If set to <span class="codeph"> zoom </span> clicking the image zooms in one zoom step; CTRL+Click zooms out one zoom step. Setting to <span class="codeph"> reset </span> causes a single click on the image to reset the zoom to the initial zoom level. For <span class="codeph"> zoomReset </span>, reset is applied if the current zoom factor is at or beyond the specified limit, otherwise zoom is applied. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Default {#section-7564169749ff4a4996049ea1148cb2a5}

`reset` on desktop computers; `zoomReset` on touch devices.

## Example {#section-96e69b70365f461dae4399e49044ea2f}

`doubleclick=zoom` 
