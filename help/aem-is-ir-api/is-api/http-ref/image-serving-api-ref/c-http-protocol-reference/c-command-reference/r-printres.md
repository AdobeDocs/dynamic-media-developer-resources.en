---
description: Print resolution. Overrides the print resolution value embedded in the response image.
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
---
# printRes{#printres}

Print resolution. Overrides the print resolution value embedded in the response image.

 `printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Print resolution (dpi). </p></td> 
 </tr> 
</table>

The print resolution is normally defined by `catalog::PrintResolution` in case of a catalog entry, otherwise by the print resolution value embedded in the source image. In case of a template or layered composite image, the default print resolution embedded in the response file is the print resolution of the layer image with the lowest layer number.

Setting the print resolution does not change the pixel size of the reply image.

## Properties {#section-03c7910ebe234804a319e5d0d8ef3a74}

Request attribute. Applies regardless of the current layer setting.

## Default {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` or the print resolution embedded in the source image.

## See also {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
