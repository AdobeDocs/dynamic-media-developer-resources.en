---
description: FavoritesView.maxloadradius
solution: Experience Manager
title: FavoritesView.maxloadradius
uuid: 0479c371-487a-4e05-b009-9036ea464abf
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
---

# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

[!DNL `[FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the component preload behavior. </p> <p>When set to <span class="codeph"> -1</span>, all thumbnails are loaded simultaneously when the component is initialized or the asset is changed. </p> <p>When set to <span class="codeph"> 0</span>, only visible thumbnails are loaded. </p> <p> When set to <span class="codeph"><span class="varname"> preloadnbr</span></span>, you can specify how many invisible rows around visible area are preloaded. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `1`]

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `maxloadradius=0`] 
