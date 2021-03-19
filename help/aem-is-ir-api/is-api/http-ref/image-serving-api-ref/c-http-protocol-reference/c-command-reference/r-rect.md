---
description: Final view rectangle. Allows the final view image to be disassembled into several strips or tiles, which can be delivered separately and reassembled by the client seamlessly, with no artifacts along the edges.
seo-description: Final view rectangle. Allows the final view image to be disassembled into several strips or tiles, which can be delivered separately and reassembled by the client seamlessly, with no artifacts along the edges.
seo-title: rect
solution: Experience Manager
title: rect
uuid: c4830fc5-d102-4789-8753-0a660d4a557e
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# rect{#rect}

Final view rectangle. Allows the final view image to be disassembled into several strips or tiles, which can be delivered separately and reassembled by the client seamlessly, with no artifacts along the edges.

 `rect= *`coord`*, *`size`*[, *`scale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>Pixel offset from the top-left corner of the view image to the top-left of the view rectangle (int, int), expressed in pixels, after <span class="varname"> scale</span> is applied. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> size</span> </p></td> 
  <td class="stentry"> <p>Size of the ROI in pixels (int, int). Specifies the reply image size. The image is filled with <span class="codeph"> bgc=</span> in areas not covered by the view image (or left transparent, if <span class="codeph"> fmt=*-alpha</span> is present in the request). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>Scale factor (real). Values smaller than 1.0 reduce the resolution, and values larger than 1.0 increase the resolution. </p></td> 
 </tr> 
</table>

Using this command, Image Serving can deliver large images via HTTP which would otherwise exceed the size limit configured with `attribute::MaxPix`.

>[!NOTE]
>
>For best results when JPEG compression is used, the strip or tile size should be a multiple of the JPEG encoding tile size (16x16 pixels).

## Example {#section-932fcfcb41d74a29bc929e4430c49601}

Separate a printable CMYK image into several full-resolution strips to reduce the download file sizes. If we were to request a contiguous image:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

First, relevant information about the image is obtained:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

The text response includes these properties:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

Based on this information, we decide that we want four 600x2000 pixel strips. The `rect=` command is used to describe the strip sizes and positions.

Since this image is changed frequently, we will include the `id=` command to minimize the chance that we end up with one or more strips from an older version of the image which may have been cached in a CDN or proxy server. The value of the `image.version` property is used for this purpose.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Properties {#section-aae223cee13e46d38b74680c048d945b}

View attribute. Applies regardless of the current layer setting.

Any areas of the ROI extending outside the view image are padded with `bgc=`.

Important `rect=` is applied *after* final scaling and fitting with `scl=`, `wid=`, `hei=`, `fit=`, `rgn=`, and `align=`.

## Default {#section-b296d3bbfb19441f87137a452b70f19a}

Entire, unmodified view image ( `rect=0,0,width,height,1.0`).

## See Also {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0) 
