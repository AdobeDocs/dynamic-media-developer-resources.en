---
description: Embed XMP metadata. Specifies whether XMP metadata should be included in the response image.
seo-description: Embed XMP metadata. Specifies whether XMP metadata should be included in the response image.
seo-title: xmpEmbed
solution: Experience Manager
title: xmpEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: c0dfd0e5-16d1-4a6e-957a-ecc276b9361a
index: y
internal: n
snippet: y
---

# xmpEmbed{#xmpembed}

Embed XMP metadata. Specifies whether XMP metadata should be included in the response image.

 `xmpEmbed=0|1`

>[!NOTE]
>
>XMP data is passed from the source image to the response image without modification. This may result in incorrect data being embedded in the response image.

## Properties {#section-27024c4272f44d9a8c264a0629193af2}

Request attribute. Ignored if the source image does not contain XMP data. Only XMP data from the source image of `layer=0` are processed. XMP data from other layer images are ignored.

Ignored if the output image format does not support XMP embedding. Refer to the description of `fmt=` for a list of output image formats that support XMP embedding.

## Default {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, for no embedding of paths in output images.

## See also {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) 
