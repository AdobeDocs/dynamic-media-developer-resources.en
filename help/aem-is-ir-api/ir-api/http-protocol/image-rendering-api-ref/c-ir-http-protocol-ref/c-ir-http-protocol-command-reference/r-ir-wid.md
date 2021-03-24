---
description: Reply image width. Specifies scaling of the rendered image so that the reply image is no taller than the specified value, while maintaining the image's aspect ratio.
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# wid{#wid}

Reply image width. Specifies scaling of the rendered image so that the reply image is no taller than the specified value, while maintaining the image's aspect ratio.

 `wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Image width in pixels (int greater than 0). </p></td> 
 </tr> 
</table>

The image is not padded if both `wid=` and `hei=` is specified and `wid`/ `hei` is different than the aspect ratio of the image.

`wid=` and `hei=` work together to define the size of the image that is returned by the server. If `scl=` comes after `wid=` or `hei=` in the URL, it cancels those commands and `scl=` defines the size of the image returned by the server.

However, if `wid=` or `hei=` comes after `scl=` in the URL, they cancel `scl=` and `wid=`/ `hei=` define the size of the image returned by the server.

>[!NOTE]
>
>An error is returned if the calculated or default reply image size is larger than `attribute::MaxPix`.

## Properties {#section-2d067c6d371748e19cb157684700a49d}

May occur anywhere within the request. Resizing the image with `wid=`, `hei=`, or `scl=` does not change the print resolution value embedded in the response image. Ignored if `scl=` occurs after `wid=` or `hei=` in the command sequence.

## Default {#section-c7c6efa03d864592a3398b6f1de5a0b0}

If neither `wid=`, `hei=`, nor `scl=` are specified, the reply image is scaled to fit within the size defined by `attribute::DefaultPix`. If `attribute::DefaultPix` is empty, the reply image will have the same size as the vignette's view image.

## See also {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attribue::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3) 
