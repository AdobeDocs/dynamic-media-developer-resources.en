---
description: null
seo-description: null
seo-title: CarouselView.enableHD
solution: Experience Manager
title: CarouselView.enableHD
topic: Dynamic media
uuid: 17df4a68-a251-427c-a3c4-1e0679e3f8f1
---

# CarouselView.enableHD{#carouselview-enablehd}

 ` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`number`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Enable, limit or disable optimization for devices where <span class="codeph"> devicePixelRatio</span> is greater than <span class="codeph"> 1</span>, that is devices with high-density display like iPhone4 and similar devices. </p> <p>If active then the component limits the size of the IS image request as if the device only had a pixel ratio of <span class="codeph"> 1</span> and that way reducing the bandwidth. </p> <p>See example below. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> number</span></span> </p> </td> 
   <td colname="col2"> <p> If using the <span class="codeph"> limit</span> setting, the component enables high pixel density only up to the specified limit. </p> <p>See example below. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always` 
