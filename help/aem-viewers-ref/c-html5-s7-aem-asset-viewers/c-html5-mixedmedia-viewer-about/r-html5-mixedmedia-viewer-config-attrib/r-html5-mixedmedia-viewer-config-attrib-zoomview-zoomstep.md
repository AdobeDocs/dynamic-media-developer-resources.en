---
description: ZoomView.zoomstep
solution: Experience Manager
title: ZoomView.zoomstep

feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5d978d21-7942-4bd6-b742-9bf4b6fd3ebe
---
# ZoomView.zoomstep{#zoomview-zoomstep}

 ` [ZoomView.|<containerId>_zoomView.]zoomstep= *`step`*[, *`limit`*]`

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

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomstep=2,3`
