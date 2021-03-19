---
description: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
uuid: 1ed18115-9e29-434a-a48d-40bf6b48fe6f
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifies image format to be used by the component for loading images from Image Server. If the specified format ends with <span class="codeph"> "-alpha"</span>, the component renders images as transparent content. For all other image formats the component treats images as opaque. Note that the component has a white background by default. Therefore, to make it completely transparent set the <span class="codeph"> background-color</span> CSS property to <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

`jpeg`

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`fmt=png-alpha` 
