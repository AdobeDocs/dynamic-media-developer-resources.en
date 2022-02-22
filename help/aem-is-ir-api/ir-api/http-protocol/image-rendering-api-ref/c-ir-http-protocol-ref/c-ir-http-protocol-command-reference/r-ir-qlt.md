---
title: qlt
description: Jpeg quality. Specifies JPEG encoding attributes to control the compression level.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
---
# qlt{#qlt}

Jpeg quality. Specifies JPEG encoding attributes to control the compression level.

 ` qlt= *`quality`*[. *`chroma`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> quality </span> </p> </td> 
  <td class="stentry"> <p>JPEG encoding quality (1…100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma </span> </p> </td> 
  <td class="stentry"> <p>JPEG chromaticity down-sampling (0=normal, 1=disable); optional, default is 0. </p> </td> 
 </tr> 
</table>

Specifies JPEG encoding attributes to control the compression level. In turn, this varies the file size (amount of the reply data), and, indirectly, the visual quality of the resultant image.

Higher *`quality`* values increase file size and quality, lower values decrease file sizes and reduce perceived image quality. Values above 90 often generate images indistinguishable from the uncompressed image.

Set the *`chroma`* flag to disable the chromaticity down-sampling employed by typical JPEG encoders. This setting may increase the perceived sharpness of edges in an image when the edge is defined by a change in hue rather than brightness. Setting this flag may cause a slight increase in file size. Experiment with this setting if text seems slightly blurry.

## Properties {#section-897b61c786dd4230a2c5807f2f40e722}

May occur anywhere in the request.

Ignored if the output image format does not support JPEG compression. Refer to the description of `fmt=` for a list of output image formats that support JPEG compression.

## Default {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## See also {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
