---
description: Resampling mode. Chooses the resampling and/or interpolation algorithm to be used for scaling image data. Also applies to rotation of text layers and resizing of composite images during the view transform.
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
---
# resMode{#resmode}

Resampling mode. Chooses the resampling and/or interpolation algorithm to be used for scaling image data. Also applies to rotation of text layers and resizing of composite images during the view transform.

 `resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Selects standard bi-linear interpolation. Fastest resampling method; some aliasing artifacts are noticeable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Selects bi-cubic interpolation. More CPU-intensive than bi-linear interpolation, but yields sharper images with less noticeable aliasing artifacts. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Selects a modified Lanczos Window function as an interpolation algorithm. Can produce slightly sharper results than bi-cubic at a higher CPU cost. <span class="codeph"> sharp </span> has been replaced by <span class="codeph"> sharp2 </span>, which has a lesser likelihood of causing aliasing artifacts (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Selects Photoshop default resampler for reducing image size which is called "bicubic sharper" in Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>To maintain the aspect ratio of an image when you use both `resMode=bisharp` and `fit=stretch`, it is best practice to use either the width parameter or the height parameter. If both parameters must be defined, you can wrap them in a different layer as shown in the following example:
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Properties {#section-a171bacf4ddf43c782e46b86a16d443e}

Request attribute. Applies to all scaling operations involved in creating the final reply image, including all layer scaling.

## Default {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Example {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Retrieve a best-quality rendition of a layered image stored in an image catalog. The image can include text. The image will be further processed in an image editing application, and thus request an alpha-channel with the image.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## See also {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
