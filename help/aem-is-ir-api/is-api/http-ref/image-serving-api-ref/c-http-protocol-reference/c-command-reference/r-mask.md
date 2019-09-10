---
description: Image mask. Specifies a separate mask image to be used as an unassociated mask.
seo-description: Image mask. Specifies a separate mask image to be used as an unassociated mask.
seo-title: mask
solution: Experience Manager
title: mask
topic: Scene7 Image Serving - Image Rendering API
uuid: 2dc14d20-f02a-4a77-9b73-0c01e10d448d
index: y
internal: n
snippet: y
---

# mask{#mask}

Image mask. Specifies a separate mask image to be used as an unassociated mask.

 `mask= *`object`*|{[is|ir]'{' *`nestedRequest`*'}'}`

<table id="simpletable_F5A8CD8D7E9B48DAB3C8184E8FE60D9B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> object</span> </p></td> 
  <td class="stentry"> <p>Image object to be used as image or layer mask. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nestedRequest</span> </p></td> 
  <td class="stentry"> <p>Nested Image Serving, Image Rendering, or external request. </p></td> 
 </tr> 
</table>

*`object`* may be either a catalog entry or an image/SVG file. Can be specified for image layers and solid color layers.

If *`object`* resolves to an image catalog entry, `catalog::MaskPath` is used, or, if `catalog::MaskPath` is not defined, then `catalog::Path` is used. If *`object`* does not resolve to a catalog entry, then it is interpreted as a file path.

In all cases, if the source image has an alpha channel, it is used. Otherwise, the image is converted to grayscale, if necessary, before using it as a layer mask.

If a mask is attached to a solid color layer, it can be cropped and scaled using the same rules used for images in image layers. `size=`, `scale=`, or `res=` can be used to scale the mask.

Layer masks can also be specified in form of a *`nestedRequest`*. Nested or embedded requests are enclosed by curly braces. Prefix an embedded Image Serving request with `is` and an embedded Image Rendering request with `ir`. A request to a foreign server is assumed if no prefix is specified. Refer to [Request Nesting and Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) for details.

## Properties {#section-a093043dc249423b8ae322cefb0d545d}

Image or layer attribute. Applies to layer 0 if `layer=comp`. Ignored by effect layers.

*`object`* must not resolve to a catalog record which includes a `src=` or `mask=` command in `catalog::Modifier`.

The `is` and `ir` prefixes are case-insensitive.

## Default {#section-10cf793c665f49deb1b248faa3b618a9}

If `mask=` is not specified explicitly, and if the layer image is associated with a catalog entry, then `catalog::MaskPath` is used. Otherwise, the alpha channel of the layer image is used, if present. If there is no alpha channel, the layer has no mask and the layer rectangle is rendered entirely opaque.

## Example {#section-1bbe623f7c744bdf97b596458d8e7ea3}

Use several separate masks to colorize different areas of an image. The colorized, masked regions is layered on top of the original, unmodified image:

`http://server/myRootId/myImageId?wid=500& layer=1&src=myImageId&mask=myMask1&op_colorize=200,0,0& layer=2&src=myImageId&mask=myMask2&op_colorize=0,200,0& layer=3&src=myImageId&mask=myMask3&op_colorize=0,0,200`

## See also {#section-7ed5201d91594e5f872438a92eaf1c89}

[maskUse=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464) , [catalog::MaskPath](r_maskpath_cat.md#reference_F82B42535FFF42959E74A7C1E605C931), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) , [Request Nesting and Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b) 
