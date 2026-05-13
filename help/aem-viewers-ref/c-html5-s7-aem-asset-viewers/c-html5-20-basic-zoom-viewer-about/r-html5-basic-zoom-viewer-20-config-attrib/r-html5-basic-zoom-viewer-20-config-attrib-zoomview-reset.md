---
title: ZoomView.reset
description: ZoomView.reset
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 054cd090-2167-4903-ba19-52bc8606370c
TQID: 'https://experienceleague.adobe.com/kQzUwh-4298IxDG436DO5AUoEOzh7vQ6bdsFqKv9q9E'
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
# ZoomView.reset{#zoomview-reset}

 `[ZoomView.|<containerId>_zoomView.]reset=0|1`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Resets the view port when frame (image) changes. If set to <span class="varname"> 0</span>, it preserves the current view port with the best possible fit while preserving the aspect ratio of the newly set image. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Default {#section-7564169749ff4a4996049ea1148cb2a5}

`1`

## Example {#section-96e69b70365f461dae4399e49044ea2f}

`reset=0`
