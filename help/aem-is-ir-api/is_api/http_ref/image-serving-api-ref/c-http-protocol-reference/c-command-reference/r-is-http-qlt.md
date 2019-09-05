---
description: JPEG quality. Specifies JPEG encoding attributes to control the compression level. This in turn varies the file size (amount of the reply data), and, indirectly, the visual quality of the resultant image.
seo-description: JPEG quality. Specifies JPEG encoding attributes to control the compression level. This in turn varies the file size (amount of the reply data), and, indirectly, the visual quality of the resultant image.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 71f98975-16d7-45e7-9b53-229a151654f6
index: y
internal: n
snippet: y
---

# qlt{#qlt}

JPEG quality. Specifies JPEG encoding attributes to control the compression level. This in turn varies the file size (amount of the reply data), and, indirectly, the visual quality of the resultant image.

 ` qlt= *`quality`*[, *`chroma`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> quality </span> </p> </td> 
  <td class="stentry"> <p>JPEG encoding quality (1…100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> chroma </span> </p> </td> 
  <td class="stentry"> <p>JPEG chromaticity down-sampling (0=normal, 1=disable); optional, default is 0. </p> </td> 
 </tr> 
</table>

Higher *`quality`* values increase file size and quality, lower values decrease file sizes and reduce perceived image quality. Values above 90 often generate images indistinguishable from the uncompressed image.

Set the *`chroma`* flag to disable the RGB chromaticity down-sampling employed by typical JPEG encoders. This may increase the perceived sharpness of edges in an image when the edge is defined by a change in hue rather than brightness. Setting this flag may cause a slight increase in file size. Experiment with this setting if text seems slightly blurry.

## Properties {#section-925a44cbdc9042db8d4eb149cd073d21}

Request attribute. Applies regardless of current layer setting. Ignored if the output image file format does not support JPEG encoding. Refer to the description of `fmt=` for information on which output image formats support `qlt=`.

*`chroma`* is ignored if the output pixel type is CMYK or gray.

## Default {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Example {#section-d7d33871d401433aa51d028823eae7a9}

Reduce quality for faster transmission over a low-bandwidth connection:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Increase quality for high-bandwidth connections:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## See also {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09) 
