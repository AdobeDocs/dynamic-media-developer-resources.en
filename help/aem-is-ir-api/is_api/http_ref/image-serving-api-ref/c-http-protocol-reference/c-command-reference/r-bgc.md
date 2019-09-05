---
description: View Background Color. Specifies the background color for the composite image (view image).
seo-description: View Background Color. Specifies the background color for the composite image (view image).
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 8a746ce5-356a-49e0-8513-ba90caaa1fd3
index: y
internal: n
snippet: y
---

# bgc{#bgc}

View Background Color. Specifies the background color for the composite image (view image).

 `bgc= *`color`*`

<table id="simpletable_998CF426296945FEA48D19E33B71A17E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span></span> </p> </td> 
  <td class="stentry"> <p>Gray, RGB, or CMYK color value. </p></td> 
 </tr> 
</table>

Specifies an opaque fill color to be used for the view background. Visible only if either the composite image has transparent areas, or if the composite image has a different aspect ratio than the view rectangle. Ignored if `fmt=tif-alpha` or `fmt=png-alpha`, or `req=mask`.

>[!NOTE]
>
>The 's' color suffix is ignored by `bgc=`. Color values specified with `bgc=` are always associated with the respective output color space.

## Properties {#section-b729b50b1ea7433b82ba34ecd61839cd}

View attribute. Applies regardless of the current layer setting. Ignored if `req=mask`, `fmt=tif-alpha`, `fmt=png-alpha`, `fmt=gif-alpha`, or `fmt=swf-alpha`.

Any alpha value specified with color is ignored.

*`color`* is assumed to belong to the output color space (as specified with `icc=`) and should have the same pixel type as the output image. If the pixel types do not match, *`color`* is converted using naïve conversion.

## Default {#section-4e025cbd723547b5ab4450f7aad70da3}

`attribute::BkgColor`.

## Example {#section-7bcdfbc0e1274e86a69d39186b090789}

Specify an explicit background color for a thumbnail request:

`http://server/myRootId/myImageId?req=tmb&bgc=214,245,130`

## See also {#section-1e55f9f98f1847918a1725836a27cfaa}

[color](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [attribute::BkgColor](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-bkgcolor.md#reference-ed53106ee50442d7a2dd3e1f60e6f0f8), [fmt=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [req=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [Color Management](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7) 
