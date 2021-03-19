---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
uuid: 8e989ca7-1ef7-4758-b6b9-c447d7647d1d
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
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
