---
description: Jpeg quality. Specifies JPEG encoding attributes to control the compression level. This in turn varies the file size (amount of the reply data), and, indirectly, the visual quality of the resultant image.
seo-description: Jpeg quality. Specifies JPEG encoding attributes to control the compression level. This in turn varies the file size (amount of the reply data), and, indirectly, the visual quality of the resultant image.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 936607c1-20c3-4f76-b970-614b21c47dea
---

# qlt{#qlt}

Jpeg quality. Specifies JPEG encoding attributes to control the compression level. This in turn varies the file size (amount of the reply data), and, indirectly, the visual quality of the resultant image.

 ` qlt= *`quality`*[, *`chroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> quality </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG encoding quality (1…100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> chroma </span> </span> </p> </td> 
  <td class="stentry"> <p>JPEG chromaticity down-sampling (0=normal, 1=disable); optional, default is 0. </p> </td> 
 </tr> 
</table>

Used only if `fmt=jpg`. Ignored otherwise

Higher quality values increase file size and quality, lower values decrease file sizes and reduce perceived image quality. Values above 90 often generate images indistinguishable from the uncompressed image.

Set the `chroma` flag to disable the RGB chromaticity down-sampling employed by typical JPEG encoders. This may increase the perceived sharpness of edges in an image when the edge is defined by a change in hue rather than brightness. Setting this flag may cause a slight increase in file size. Experiment with this setting if text seems slightly blurry.

`chroma` is ignored if the output pixel type is CMYK or gray.

## Example {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80] 
