---
description: Swatches.align
solution: Experience Manager
title: Swatches.align

feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3cb91483-de8c-4d5c-9b46-7026c5001f3a
---
# Swatches.align{#swatches-align}

 `[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Specifies the internal alignment (anchoring) of the swatches container within the component area. In Swatches, the internal thumbnail container is sized so that only a whole number of swatches is shown. As a result, there is some padding between internal container and external component bounds. This command specifies how the internal swatches container is positioned inside component.

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> left|center|right</span> </p> </td> 
   <td> <p> Sets the alignment of the horizontal swatches. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
   <td> <p> Sets the alignment of the vertical swatches. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`center,center`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`align=left,top`
