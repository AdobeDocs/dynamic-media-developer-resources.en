---
description: SpinView.zoomstep
solution: Experience Manager
title: SpinView.zoomstep

feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
exl-id: 919477d0-87d9-4cf7-a7c8-0fbb68c6ff96
---
# SpinView.zoomstep{#spinview-zoomstep}

 ` [SpinView.|<containerId>_spinView.]zoomstep= *`step`*[, *`limit`*]`

<table id="table_1D425B7685D448459CD3FE8D683C813C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p> Configures the number zoom in and zoom out actions that are required to increase or decrease the resolution by a factor of two. The resolution change for each zoom action is 2^1 per step. Set to <span class="codeph"> 0</span> to zoom to full resolution with a single zoom action. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> limit</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the maximum zoom resolution, relative to the full resolution image. The default is <span class="codeph"> 1.0</span>, which does not allow zooming beyond full resolution. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Default {#section-7a2128fd488941948aff18421f533ccf}

`1,1`

## Example {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`zoomstep=2,3`
