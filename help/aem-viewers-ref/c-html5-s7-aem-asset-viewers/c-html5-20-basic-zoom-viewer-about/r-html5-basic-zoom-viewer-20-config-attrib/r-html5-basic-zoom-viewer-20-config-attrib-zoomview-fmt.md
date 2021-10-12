---
title: ZoomView.fmt
description: ZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 7cb75d38-a577-4e06-b679-c4e00db5059a
---
# ZoomView.fmt{#zoomview-fmt}

 `[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifies the image format that the component uses for loading images from Image Server. If the specified format ends with "-alpha ", the component renders images as transparent content. For all other image formats the component treats images as opaque. The component has a white background by default. Therefore, to make it transparent, set the background-color CSS property to transparent. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Default {#section-7564169749ff4a4996049ea1148cb2a5}

`jpeg`

## Example {#section-96e69b70365f461dae4399e49044ea2f}

`fmt=png-alpha`
