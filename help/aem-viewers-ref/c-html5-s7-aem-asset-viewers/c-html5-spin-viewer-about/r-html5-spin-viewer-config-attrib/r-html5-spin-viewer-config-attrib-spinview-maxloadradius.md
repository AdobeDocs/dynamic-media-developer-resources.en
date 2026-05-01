---
title: SpinView.maxloadradius
description: SpinView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4adba865-0b03-469e-a88c-2c3982422a68
TQID: https://experienceleague.adobe.com/6gb07GIU34p3ieAvHSqoM5G0d-9g8-EdIEzBMDcHO3M
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# SpinView.maxloadradius{#spinview-maxloadradius}

 ` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Represents the maximum number of frames to preload in each direction when the SpinView is idle. A value of <span class="codeph"> -1</span> preloads all frames in the set. The preloaded frames are always seen at the original resolution that the SpinView was initially loaded. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controls the quality of preloaded frames. When set to <span class="codeph"> 1</span> frames load in high-quality, matching the size of the component. When set to <span class="codeph"> 0</span> only the low-resolution preview tile is loaded. </p> <p>Preloading in high resolution improves the end-user experience, especially when auto-spin is enabled. At the same time, it results in slower start time and higher network consumption, so use with caution. When a high-resolution preload is used, the preloaded frames are always at the original resolution that the component was initially loaded at. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Default {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Example {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
