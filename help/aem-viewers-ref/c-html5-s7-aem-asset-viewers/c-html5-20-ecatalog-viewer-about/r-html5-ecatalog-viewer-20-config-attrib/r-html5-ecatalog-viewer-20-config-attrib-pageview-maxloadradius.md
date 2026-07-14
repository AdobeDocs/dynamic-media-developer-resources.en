---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 02925e09-f1ab-4afb-a900-d216efd323fe
TQID: 'https://experienceleague.adobe.com/BTz86cHc382RcPQ%2D%2D%2DRcZqenmf5Dm5zKsbtJizSE6-U'
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
# PageView.maxloadradius{#pageview-maxloadradius}

`[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Specifies the component preload behavior. </p> <p>When set to <span class="codeph"> -1</span> the component preloads all the catalog frames when in an idle state. </p> <p> When set to <span class="codeph"> 0</span> the component loads only the frame that is currently visible, previous, and next frame. </p> <p>Set <span class="codeph"><span class="varname"> preloadnbr</span></span> to define how many invisible frames around the currently displayed frame are preloaded in an idle state. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-4b7952997f9240e581d21bcdb173f9af}

Optional.

## Default {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## Example {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
