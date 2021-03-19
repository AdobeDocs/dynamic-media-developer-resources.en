---
description: View width. Specifies the width of the response image (view image) when fit= is not present in the request.
seo-description: View width. Specifies the width of the response image (view image) when fit= is not present in the request.
seo-title: wid
solution: Experience Manager
title: wid
uuid: 30aeeea0-c8c9-40b9-a244-2802a7102dd6
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# wid{#wid}

View width. Specifies the width of the response image (view image) when fit= is not present in the request.

 ` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Image width in pixels (int greater than 0). </p> </td> 
 </tr> 
</table>

If both `hei=` and `scl=` are specified, the composite image may be cropped according to the `align=` attribute. When `fit=` is present, `wid=` specifies the exact, the minimum, or the maximum response image width; refer to the description of `fit=` for details.

If `scl=` is not specified, the composite image is scaled to fit. If both `wid=` and `hei=` are specified, and `scl=` is not specified, then the image is scaled to fit entirely within the wid/hei rectangle, leaving as little background area exposed as possible. In this case, the image is positioned within the view rectangle according to the `align=` attribute.

>[!NOTE]
>
>An error is returned if the calculated or default reply image size is larger than `attribute::MaxPix`.

## Default {#section-976d4c8554a34c899f85d172f6ac6f58}

If neither `wid=`, `hei=`, nor `scl=` are specified, the reply image will either have the size of the composite image or `attribute::DefaultPix`, whichever is smaller.

## Properties {#section-c93b7ce1b0d2475f80b06264b45d1285}

View attribute. Applies regardless of the current layer setting.

## Example {#section-82bc98b7c15a451bbe9b915d414c0470}

Request an image to fit into a 200x200 rectangle; top-right align the image if it is not square. Any background area is filled with `attribute::BkgColor`.

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

The same image, delivered at a fixed width of 200 pixels, but with a variable height to maintain the aspect ratio of the image. In this case, the returned image never has any background fill areas. Note that in this case align= would have no effect at all.

` http:// *`server`*/myRootId/myImageId?wid=200`

## See also {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5) 
