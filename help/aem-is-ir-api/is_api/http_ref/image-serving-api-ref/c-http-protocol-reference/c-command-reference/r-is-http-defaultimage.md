---
description: Default Reply Image. Specifies the image or catalog entry to be used when an image cannot be found.
seo-description: Default Reply Image. Specifies the image or catalog entry to be used when an image cannot be found.
seo-title: defaultImage
solution: Experience Manager
title: defaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: 2e3dc94a-fd07-4b4c-89d5-9d0599d82cd5
index: y
internal: n
snippet: y
---

# defaultImage{#defaultimage}

Default Reply Image. Specifies the image or catalog entry to be used when an image cannot be found.

 ` defaultImage= *`object`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> object </span> </span> </p> </td> 
  <td class="stentry"> <p>Image object. </p> </td> 
 </tr> 
</table>

*`object`* may be either a catalog entry (including a template) or a simple image file path. Useful for substituting missing images with default images. This value overrides the value of the corresponding catalog `attribute::DefaultImage`. An empty value ( `defaultImage=`) disables default image handling.

>[!NOTE]
>
>The default image mechanism does not apply to SVG objects. An error is returned if the SVG object specified in the request cannot be found.

If `attribute::DefaultImageMode=0`, *`object`* replaces the entire original request, even if only one image in a multi-image composition is missing. The only commands retained from the original request are: `wid=`, `hei=`, `fmt=`, `qlt=`.

If `attribute::DefaultImageMode=1`, object replaces only the missing layer image; attributes for the missing layer are applied and the composite is processed and returned as usual.

## Properties {#section-d30923d8dc4042eba10989212dd70887}

Request attribute. Applies regardless of the current layer setting. Ignored if `req=` is other than `img` or `tmb`.

## Restrictions {#section-30df31bc8cac41cd917f1e45196779c2}

Foreign image sources are not covered by the default image mechanism; an error is returned if a foreign image source is not valid.

Image Serving reverts back to `DefaultImageMode=0` when nested Image Rendering or FXG render requests fail.

## Default {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## See also {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [attribute:: DefaultImage](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [ *`object`* ](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) 
