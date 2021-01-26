---
description: Configuration attribute for Interactive Video Viewer.
seo-description: Configuration attribute for Interactive Video Viewer.
seo-title: CallToAction.maxloadradius
solution: Experience Manager
title: CallToAction.maxloadradius
topic: Dynamic Media
uuid: ec5a4b0d-1dae-456f-a9da-91541cfba1a7
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

