---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
TQID: https://experienceleague.adobe.com/xSgRsT0-xd0Af7hkZBnWeM5QoY2Ge0wWvEZAvOmZso4
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|dotted</span> </p> </td> 
   <td colname="col2"> <p> Configures the rendering style of the set indicator. </p> <p>When set to <span class="codeph"> dotted </span>, the component renders identical indicators for all pages. </p> <p>When set to <span class="codeph"> numeric</span> it puts a 1-based page number inside each indicator element. </p> <p>The <span class="codeph"> numeric</span> operation mode is not supported on devices that have touch input. Instead, the component uses <span class="codeph"> dotted</span> on such devices. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
