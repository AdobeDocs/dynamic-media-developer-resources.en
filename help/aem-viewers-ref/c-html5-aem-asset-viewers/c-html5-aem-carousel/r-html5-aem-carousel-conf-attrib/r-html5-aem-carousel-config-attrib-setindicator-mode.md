---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
---
# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|dotted</span> </p> </td> 
   <td colname="col2"> <p> Configures the rendering style of the set indicator. </p> <p>When set to <span class="codeph"> dotted</span> the component renders identical indicators for all pages. </p> <p>When set to <span class="codeph"> numeric</span> it puts a 1-based page number inside each indicator element. </p> <p>The <span class="codeph"> numeric</span> operation mode is not supported on devices that are capable of touch input. Instead, the component uses <span class="codeph"> dotted</span> on such devices. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
