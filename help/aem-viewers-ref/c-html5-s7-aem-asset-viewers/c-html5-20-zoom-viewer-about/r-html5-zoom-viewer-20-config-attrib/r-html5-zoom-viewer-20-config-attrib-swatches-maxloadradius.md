---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: df9d5be4-d1e1-4b72-a7e7-0f3611278d2a
TQID: 'https://experienceleague.adobe.com/lx-kygwnrE26h0YA1tPfv59apt-uJMYSh2shtavHo-Q'
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
# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Specifies the component preload behavior. When set to <span class="codeph"> -1</span> all swatches are loaded simultaneously when the component is initialized or the asset is changed. </p> <p>When set to <span class="codeph"> 0</span> only visible swatches are loaded. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> defines how many invisible rows/columns around the visible area are preloaded. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`1`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=-1`

