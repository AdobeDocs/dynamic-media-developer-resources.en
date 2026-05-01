---
title: CallToAction.maxloadradius
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
TQID: https://experienceleague.adobe.com/Y-bGQIlV8mjCEpUtvUiXWmZl8Ev6LzKrm6yGe2O7eMk
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Configuration attribute for Interactive Video Viewer.

 ` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the component preload behavior. </p> <p>When set to <span class="codeph"> -1</span> all the thumbnails are loaded simultaneously when the component is initialized or the asset is changed. </p> <p>When set to <span class="codeph"> 0</span> only visible thumbnails are loaded. </p> <p>Set to <span class="codeph"><span class="varname"> preloadnbr</span></span> to define how many invisible rows/columns around the visible area are preloaded. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`-1`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
