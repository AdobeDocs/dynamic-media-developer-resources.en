---
title: ZoomView.zoomstep
description: ZoomView.zoomstep
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: bcd153f3-7a87-4e8f-825b-fc4a136de1dc
TQID: 'https://experienceleague.adobe.com/7wu--abb-d3xqm2uJzgyubkb7SmaDVStd0-oCNEXYqc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`1,1`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`zoomstep=2,3`

