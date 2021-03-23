---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius

feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
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
