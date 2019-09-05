---
description: Layer image.
seo-description: Layer image.
seo-title: src
solution: Experience Manager
title: src
topic: Scene7 Image Serving - Image Rendering API
uuid: c09c0359-795c-48e8-a922-122a70409003
index: y
internal: n
snippet: y
---

# src{#src}

Layer image.

 ` src= *`object`*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> object </span> </p> </td> 
  <td class="stentry"> <p>Image object. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>Nested Image Serving, Image Rendering, or external request. </p> </td> 
 </tr> 
</table>

## Description {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Specifies the source image for an image layer.

*`object`* may be either a catalog entry or an image/SVG file.

See [object](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Nested or embedded requests are enclosed by curly braces. Prefix an embedded Image Serving request with `is`, an embedded Image Rendering request with `ir`, and an FXG graphics render request with `fxg`. A request to a foreign server is assumed if no prefix is specified.

See [Request Nesting and Embedding](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

>[!NOTE]
>
>FXG graphics rendering is available only in the Scene7 hosted environment and may require additional licensing. Contact Scene7 Support for more information.

## Properties {#section-2c22bb89a35d470f833df8ba898efd93}

Layer attribute. Applies to `layer=0` if `layer=comp`. Mutually exclusive with `text=` and `textPs=` in the same layer; the last occurrence of either `text=`, `textPs=`, or `src=` prevails and determines whether this is an image or a text layer. Ignored by effect layers.

*`object`*may not resolve to another catalog record which includes a `src=` or `mask=` command in its `catalog::Modifier`. (Use request nesting to achieve a similar effect.)

The `is`, `ir`, and `fxg` prefixes are case-sensitive.

## Default {#section-a92f3882041b4d43ae2caf014647165f}

For layer 0 the object from the path component of the URL is used if `src=` is not specified. No default value for other layers.

## See also {#section-e467e03330564796932ac081f1c9c1d0}

[catalog::Path](r_path_cat.md#reference_306AFCAFF172440CA81B85DA8D78213C) , [attribute::RootPath](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [text=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textPs=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [mask=](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [object](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Templates](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Request Nesting and Embedding](../../../../../is_api/http_ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) 
