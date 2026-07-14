---
title: ThumbnailGridView.fmt
description: ThumbnailGridView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 916ee5d1-e398-4923-9107-96f649033298
TQID: 'https://experienceleague.adobe.com/Jp3-9jcSw3-AnFXY4TXdJrXdaKNQB-F5lPAYMcDl8uI'
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
# ThumbnailGridView.fmt{#thumbnailgridview-fmt}

 `[ThumbnailGridView.|<containerId>_gridView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Specifies the image format that the component uses for loading images from Image Server. It can be any value that Image Server and the client browser supports. If the specified format ends with <span class="codeph"> -alpha</span>, the component renders images as transparent content. For all other image formats the component treats images as opaque. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-ffe8ccc3a5f2474db47a68c2ad9a96d6}

Optional.

## Default {#section-502c098dbae1452180c7f575a1d9dc8b}

`jpeg`

## Example {#section-5cde7b856ba646c293cfd3d79e47c507}

`fmt-png-alpha`

