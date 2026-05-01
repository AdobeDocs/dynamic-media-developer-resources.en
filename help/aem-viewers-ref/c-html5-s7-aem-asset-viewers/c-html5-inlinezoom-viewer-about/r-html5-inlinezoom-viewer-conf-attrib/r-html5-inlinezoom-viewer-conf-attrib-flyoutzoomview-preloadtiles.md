---
title: FlyoutZoomView.preloadtiles
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: f50ea45a-afd5-4e4f-967d-c45cecc5fb7b
TQID: https://experienceleague.adobe.com/l0p5g4X23iHZZlJ3JUzkWWKNiL-Gkadnj56W78O0l6c
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

 `[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Set to <span class="codeph"> 1</span> to enable preloading of the zoomed image, or set to <span class="codeph"> 0</span> to load the zoom image incrementally, as needed. </p> <p> <p>Note:  If you enable this option it can result in substantially higher bandwidth usage. The zoomed image is loaded in its entirety, even if the user does not initiate a zoom action. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Default {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## Example {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
