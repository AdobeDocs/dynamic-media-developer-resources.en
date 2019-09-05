---
description: Reply image height. Specifies scaling of the rendered image so that the height of the reply image is no larger than the specified value, while maintaining the image's aspect ratio.
seo-description: Reply image height. Specifies scaling of the rendered image so that the height of the reply image is no larger than the specified value, while maintaining the image's aspect ratio.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 730a16f4-f169-4146-91cb-ad781047e88e
index: y
internal: n
snippet: y
---

# hei{#hei}

Reply image height. Specifies scaling of the rendered image so that the height of the reply image is no larger than the specified value, while maintaining the image's aspect ratio.

 `hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Reply image height in pixels (integer greater than 0). </p></td> 
 </tr> 
</table>

The image is not padded if both `wid=` and `hei=` are specified and width/height is different than the aspect ratio of the image.

`wid=` and `hei=` work together to define the size of the image that is returned by the server. If `scl=` comes after `wid=` or `hei=` in the URL, it cancels those commands and `scl=` defines the size of the image returned by the server.

However, if `wid=` or `hei=` comes after `scl=` in the URL, they cancel `scl=` and `wid=`/ `hei=` define the size of the image returned by the server.

>[!NOTE]
>
>An error is returned if the calculated or default reply image size is larger than `attribute::MaxPix`.

## Properties {#section-6cbc6acd37c847beab84c896ac25280c}

May occur anywhere within the request. Resizing the image with `wid=`, `hei=`, or `scl=` does not change the print resolution value embedded in the response image. Ignored if `scl=` occurs after `wid=` and/or `hei=` in the command sequence.

## Default {#section-61043f6c1f5d450883ff9e5eafd95955}

If neither `wid=`, `hei=`, nor `scl=` are specified, the reply image is scaled to fit within the size defined by `attribute::DefaultPix`. If `attribute::DefaultPix` is empty, the reply image has the same size as the vignette's view image.

## See also {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute::DefaultPix](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribute::MaxPix](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3) 
