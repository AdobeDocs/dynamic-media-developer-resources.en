---
title: FavoritesView.favoritesThumbView
description: FavoritesView.favoritesThumbView
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 5c57fcc8-be67-408a-9c4c-4e15d5fe6410
TQID: 'https://experienceleague.adobe.com/o1SjDLDUYHn7ygVPxi5Af7ElhXgISpmoFANSuMf0xNk'
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
# FavoritesView.favoritesThumbView{#favoritesview-favoritesthumbview}

` [FavoritesView.|<containerId>_favoritesView.]favoritesThumbArea= *`area`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> area</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the crop area for Favorites thumbnail. Expressed as a relative value to the total frame size, with a range from <span class="codeph"> 0</span> to <span class="codeph"> 1.0</span>. </p> <p>A value of <span class="codeph"> 1</span> means that the entire frame image is used for the thumbnail. </p> <p>A value of <span class="codeph"> 0.1</span> means only 10% of the frame size is used. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`0.1`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`favoritesThumbArea=0.5`
