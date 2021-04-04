---
description: PageView.zoomstep
solution: Experience Manager
title: PageView.zoomstep

feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
exl-id: d92e56ae-2bb6-46f6-b0f7-64b867492a37
---
# PageView.zoomstep{#pageview-zoomstep}

  [!DNL `[PageView.|<containerId>_pageView.]zoomstep= *`step`*[, *`limit`*]`]

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p> Configures the number of zoom in and zoom out actions that are required to increase or decrease the resolution by a factor of two. The resolution change for each zoom action is 2^1 per step. Set to <span class="codeph"> 0</span> to zoom to full resolution with a single zoom action. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> limit</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the maximum zoom resolution, relative to the full resolution image. The default is <span class="codeph"> 1.0</span>, which does not allow zooming beyond full resolution. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-636d35a4791447039f1902973f568320}

Optional.

## Default {#section-ad8a5fe2383e4c228bf177a41b53d921}

[!DNL `1,1`]

## Example {#section-1e20672d42c845bd84f02f88cbc53efc}

[!DNL `zoomstep=2,3`]
