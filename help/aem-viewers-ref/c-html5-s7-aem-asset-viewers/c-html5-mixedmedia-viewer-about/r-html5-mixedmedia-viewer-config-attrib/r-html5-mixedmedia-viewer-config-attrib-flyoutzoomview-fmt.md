---
description: Specifies the image format that the component uses for loading images from Image Server.


solution: Experience Manager
title: FlyoutZoomView.fmt

feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,Business Practitioner
exl-id: 6e3bf609-eae7-4db9-b922-cba3a9f7634b
---
# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Specifies the image format that the component uses for loading images from Image Server.

 `[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> If the specified format ends with <span class="codeph"> -alpha</span>, the component renders images as transparent content. For all other image formats, the component treats images as opaque. </p> <p>Note that the component has a white background by default. Therefore, to make it completely transparent, set the <span class="codeph"> background-color</span> CSS property to <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
