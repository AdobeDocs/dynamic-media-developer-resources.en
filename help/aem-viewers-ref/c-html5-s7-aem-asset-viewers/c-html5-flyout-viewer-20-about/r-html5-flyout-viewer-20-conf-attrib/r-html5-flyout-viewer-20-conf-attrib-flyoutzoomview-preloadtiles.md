---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
topic: Dynamic Media
uuid: e73f9d5d-4b7a-4a6b-8d0f-a5e588dc00c9
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

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`preloadtiles=1` 
