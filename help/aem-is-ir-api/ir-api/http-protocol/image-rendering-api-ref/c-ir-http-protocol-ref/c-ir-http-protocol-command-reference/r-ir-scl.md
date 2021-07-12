---
description: Scale view. Scales the rendered image by the specified scale factor, relative to the full-resolution vignette.
solution: Experience Manager
title: scl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
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

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
