---
description: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt

feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifies image format to be used by the component for loading images from Image Server. If the specified format ends with <span class="codeph"> -alpha</span>, the component renders images as transparent content. For all other image formats the component treats images as opaque. </p> <p>Note that the component has a white background by default. Therefore, to make it completely transparent set the <span class="codeph"> background-color</span> CSS property to <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Default {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## Example {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha` 
