---
description: ThumbnailGridView.maxloadradius
solution: Experience Manager
title: ThumbnailGridView.maxloadradius

feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
---

# ThumbnailGridView.maxloadradius{#thumbnailgridview-maxloadradius}

` [ThumbnailGridView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_D29F1F6A8EC74F42A254C823435F9493"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Specifies the component preload behavior. </p> <p>When set to <span class="codeph"> -1</span> the thumbnails are loaded simultaneously when the component is initialized or the asset changes. </p> <p>When set to <span class="codeph"> 0</span> only the visible thumbnails are loaded. </p> <p>Set <span class="codeph"><span class="varname"> preloadnbr</span></span> defines how many invisible rows/columns around the visible area are preloaded. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-a3abd04c03e14c238a07349ce50d8310}

Optional.

## Default {#section-c60e81667965460cbf03378a1ab9b187}

`1`

## Example {#section-472614b59e04430490a7f16c932bce89}

`maxloadradius=0` 
