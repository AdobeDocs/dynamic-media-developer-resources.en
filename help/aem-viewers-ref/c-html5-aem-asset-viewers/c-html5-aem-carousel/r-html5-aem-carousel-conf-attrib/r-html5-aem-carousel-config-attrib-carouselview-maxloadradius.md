---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius

feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Specifies the component preload behavior. </p> <p>When set to <span class="codeph"> -1</span> the component will preload all carousel frames when in an idle state. </p> <p>When set to <span class="codeph"> 0</span> the component loads only the frame that is currently visible, previous, and next frame. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span>defines how many invisible frames around the currently displayed frame are preloaded when in an idle state. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`1`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0` 
