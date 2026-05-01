---
title: Swatches.direction
description: Swatches.direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 8294c9f0-4c4e-4095-beeb-94d8dcfc2cd7
TQID: https://experienceleague.adobe.com/IP6PTQ95WbDXuRQzoLW-Ow9KNjkadEkbDUOt6yQhSew
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Swatches.direction{#swatches-direction}

 `[Swatches.|<containerId>_swatches.]direction=auto|left|right`

<table id="table_8DA8AC17A6FB4EC09DC9384B812D841C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Specifies the way swatches fill in the view. </p> <p> <span class="codeph"> left </span> sets left-to-right fill order; <span class="codeph"> right </span> reverses the order so that the view is filled in right-to-left, top-to-bottom direction. When <span class="codeph"> auto </span> is set, the component applies right mode when locale is set to <span class="codeph"> "ja" </span>, and uses left otherwise. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Default {#section-fcb06fd8e7e945e590094efcf9a1d510}

`auto`

## Example {#section-3a188ab955c445bcb2efa3c49722c10d}

`direction=right`
