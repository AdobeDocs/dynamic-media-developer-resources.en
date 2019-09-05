---
description: View Height. Specifies the height of the response image (view image) when fit is not present in the request.
seo-description: View Height. Specifies the height of the response image (view image) when fit is not present in the request.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 96a007e1-2b91-40d4-a731-34e34a2fbc6e
index: y
internal: n
snippet: y
---

# hei{#hei}

View Height. Specifies the height of the response image (view image) when fit is not present in the request.

 ` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Image height in pixels (int greater than 0). </p> </td> 
 </tr> 
</table>

If both `wid=` and `scl=` are specified, the composite image may be cropped according to the `align=`attribute. When `fit=` is present, `hei=` specifies the exact, the minimum, or the maximum response image height; refer to the description of ` [fit=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)` for details.

If `scl=` is not specified, the composite image is scaled to fit. If both `wid=` and `hei=` are specified, and `scl=` is not specified, then the image is scaled to fit entirely within the wid/hei rectangle, leaving as little background area exposed as possible; in this case, the image is positioned within the view rectangle according to the `align=` attribute. The background area is filled with `bgc=`, or, if not specified with `attribute::BkgColor`.

>[!NOTE]
>
>An error is returned if the calculated reply image size is larger than `attribute::MaxPix`.

## Properties {#section-534923644a1e464496eeba83dedcbd3c}

View attribute. Applies regardless of the current layer setting.

## Default {#section-76544d34806d4124a8b173e229cba71f}

If neither `wid=`, `hei=`, nor `scl=` are specified, the reply image has either the size of the composite image or `attribute::DefaultPix`, whichever is smaller.

## Examples {#section-eb10df7cd67e4733984810aaffd0b9e2}

Request an image to fit into a 200x200 rectangle; top-left align the image if it is not square. Any background area is filled with `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

The same image, delivered at a fixed height of 200 pixels, but with a variable width to match the aspect ratio of the image. In this case, the returned image never has any background fill areas. Note that in this case `align=` would have no effect at all.

`http://server/myRootId/myImageId?hei=200`

## See also {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [fit=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [bgc=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [rgn=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::DefaultPix](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5) 
