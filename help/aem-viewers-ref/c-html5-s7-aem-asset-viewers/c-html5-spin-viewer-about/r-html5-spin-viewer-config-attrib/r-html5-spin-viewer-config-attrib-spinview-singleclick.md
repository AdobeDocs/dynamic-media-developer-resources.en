---
description: SpinView.singleclick
solution: Experience Manager
title: SpinView.singleclick

feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
---
# SpinView.singleclick{#spinview-singleclick}

 `[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configures the mapping of single-click/tap to zoom actions. Setting to <span class="codeph"> none </span> disables single-click/tap zoom. If set to <span class="codeph"> spin </span> clicking the image zooms in one zoom step; CTRL+Click zooms out one zoom step. Setting to <span class="codeph"> reset </span> causes a single click on the image to reset the zoom to the initial spin level. For <span class="codeph"> zoomReset </span>, reset is applied if the current zoom factor is at or beyond the specified limit, otherwise zoom is applied. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Default {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` on desktop computers; `none` on touch devices.

## Example {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
