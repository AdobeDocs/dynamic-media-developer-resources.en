---
description: Thumbnail type. Describes how a thumbnail for this image is to be generated.
seo-description: Thumbnail type. Describes how a thumbnail for this image is to be generated.
seo-title: ThumbType
solution: Experience Manager
title: ThumbType
topic: Scene7 Image Serving - Image Rendering API
uuid: b737b5a4-ad6d-4a9c-b48f-81cf170dd210
---

# ThumbType{#thumbtype}

Thumbnail type. Describes how a thumbnail for this image is to be generated.

 The following thumbnail types are supported:

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Crop (1) </p></td> 
  <td class="stentry"> <p>Crop the image to the thumbnail aspect ratio. Unless the aspect ratio of the thumbnail rectangle and the image are exactly the same, a part of the image ise cropped to ensure that the entire thumbnail rectangle is filled with image data. The crop rectangle is positioned in the image using <span class="codeph"> attribute::ThumbHorizAlign</span> and <span class="codeph"> attribute::ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Fit (2) </p></td> 
  <td class="stentry"> <p>Fit the entire image into the thumbnail rectangle. The image is positioned within the thumbnail rectangle using <span class="codeph"> attribute::ThumbHorizAlign</span> and <span class="codeph"> attribute::ThumbVertAlign</span>, and any extra space is filled with <span class="codeph"> attribute::ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Texture (3) </p></td> 
  <td class="stentry"> <p>Crop the image based on resolution. The image is scaled by ratio of <span class="codeph"> catalog::ThumbRes</span> to <span class="codeph"> catalog::Resolution</span>. If the resulting image is larger than the thumbnail, it is cropped to fit, if the scaled image is smaller than the thumbnail, the remaining area is filled with <span class="codeph"> attribute::ThumbBkgColor</span>. <span class="codeph"> attribute::ThumbHorizAlign</span> and <span class="codeph"> attribute::ThumbVertAlign</span> are used to determine the position of the crop rectangle within a larger image or position of a smaller image within the thumbnail. </p></td> 
 </tr> 
</table>

Clients request image thumbnails with `req=tmb` requests.

## Properties {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Enum Value. Valid values are 1, 2, or 3, which corresponds to Crop, Fit, and Texture types, respectively.

## Default {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` is used if the field is not present, if the value is 0 or if the field is empty.

## See also {#section-fc1a79d3e6274b4381a17da159649a07}

[attribute::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) , [attribute::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e), [attribute::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691), [attribute::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f), [catalog::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69), [catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f) 
