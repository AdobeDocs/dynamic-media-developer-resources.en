---
title: FavoritesView.fmt
description: FavoritesView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d14f8a0c-5fb5-4315-ba8b-79add6d389b0
---
# FavoritesView.fmt{#favoritesview-fmt}

`[FavoritesView.|<containerId>_favoritesView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifies the image format used by the component for loading images from Image Server. The format is any value that is supported by the Image Server and the client browser. </p> <p>If the image format ends with <span class="codeph"> -alpha</span>, the component renders the images as transparent content. For all other image format values, the component treats images as opaque. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`jpeg`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`fmt=png-alpha`
