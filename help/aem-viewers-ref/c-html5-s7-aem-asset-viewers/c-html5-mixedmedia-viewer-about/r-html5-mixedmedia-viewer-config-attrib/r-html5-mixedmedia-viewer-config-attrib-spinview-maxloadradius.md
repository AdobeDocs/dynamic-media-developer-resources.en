---
description: Represents the maximum number of frames to preload in each direction when the SpinView is idle.
seo-description: Represents the maximum number of frames to preload in each direction when the SpinView is idle.
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic Media
uuid: e1b9fa84-837c-465e-8d37-0b6867404cae
---

# SpinView.maxloadradius{#spinview-maxloadradius}

Represents the maximum number of frames to preload in each direction when the SpinView is idle.

 ` [SpinView.|<containerId>_spinView.]maxloadradius= *`value`*[, *`highRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> A value of <span class="codeph"> -1</span> preloads all frames in the set. The preloaded frames are always seen at the original resolution that the SpinView was initially loaded. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Controls the quality of preloaded frames. </p> <p>When set to <span class="codeph"> 1</span> the frames load in high-quality, matching the size of the component. </p> <p>When set to <span class="codeph"> 0</span> only the low-resolution preview tile is loaded. </p> <p>Preloading in high resolution improves end user experience, especially when auto-spin is enabled. At the same time, it results in slower start time and higher network consumption, so it should be used with care. When high-resolution preload is used, the preloaded frames are always in the original resolution at which the component was initially loaded. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1` 
