---
description: Scale view. Scales the rendered image by the specified scale factor, relative to the full-resolution vignette.
seo-description: Scale view. Scales the rendered image by the specified scale factor, relative to the full-resolution vignette.
seo-title: scl
solution: Experience Manager
title: scl
topic: Scene7 Image Serving - Image Rendering API
uuid: e79e4518-af80-4619-bccc-e79f42275da5
index: y
internal: n
snippet: y
---

# scl{#scl}

Scale view. Scales the rendered image by the specified scale factor, relative to the full-resolution vignette.

 `scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>Inverse scale factor (real, 1.0 or greater). </p></td> 
 </tr> 
</table>

If `scl=` comes after `wid=` or `hei=` in the URL, it cancels those commands and `scl=` defines the size of the image returned by the server.

However, if `wid=` or `hei=` comes after `scl=` in the URL, they cancel `scl=` and `wid=`/ `hei=` define the size of the image returned by the server.

>[!NOTE]
>
>An error is returned if the calculated or default reply image size is larger than `attribute::MaxPix`.

## Properties {#section-170458cbd6984bd59a3434431258b20f}

May occur anywhere within the request. Ignored if `wid=` or `hei=` occur after `scl=` in the command sequence.

Resizing the image with `scl=` does not change the print resolution value embedded in the response image.

## Default {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

If neither `wid=`, `hei=` nor `scl=` are specified, the reply image is scaled to fit within the size defined by `attribute::DefaultPix`. If `attribute::DefaultPix` is empty, the reply image has the same size as the vignette's view image.

## See also {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [attribute::MaxPix](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [attribute::DefaultPix](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) 
