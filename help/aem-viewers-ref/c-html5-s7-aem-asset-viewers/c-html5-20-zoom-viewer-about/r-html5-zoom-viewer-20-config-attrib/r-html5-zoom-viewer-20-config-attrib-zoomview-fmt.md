---
description: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
uuid: 8e3e16a8-7b3c-4cb0-9c6d-a067bc7f6191
feature: "Dynamic Media Classic,Viewers,SDK/API,Zoom"
role: "Developer,Business Practitioner"
---

# ZoomView.fmt{#zoomview-fmt}

 `[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifies the image format that the component uses for loading images from Image Server. If the specified format ends with <span class="codeph"> -alpha</span>, the component renders images as transparent content. For all other image formats the component treats images as opaque. The component has a white background by default. Therefore, to make it transparent, set the <span class="codeph"> background-color</span> CSS property to <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha` 
