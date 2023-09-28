---
title: PanoramicView.fmt
description: Specifies the image format used by the component for loading images from Image Server.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
---
# PanoramicView.fmt{#panoramicview-fmt}

Specifies the image format used by the component for loading images from Image Server. If the specified format ends with "-alpha", the component renders the images as transparent. For all other image formats, the component treats images as opaque. The component has a transparent background by default. Therefore, to make it opaque, set the `background-color` CSS property to `desired_color`

 `[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> Specifies the image format to be used by the component for loading images from Image Server. If the specified format ends with "-alpha", the component renders images as transparent content; for all other image formats the component treats images as opaque. The component has a transparent background by default. Therefore, to opaque, set the background-color CSS property to the desired color. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
