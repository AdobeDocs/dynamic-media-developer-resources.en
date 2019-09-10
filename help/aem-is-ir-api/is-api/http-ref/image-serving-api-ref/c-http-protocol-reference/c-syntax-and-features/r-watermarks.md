---
description: Image Serving implements a simple visual watermarking facility.
seo-description: Image Serving implements a simple visual watermarking facility.
seo-title: Watermarks
solution: Experience Manager
title: Watermarks
topic: Scene7 Image Serving - Image Rendering API
uuid: b2bbaa59-dad9-4be3-bb92-142ed44f6d65
index: y
internal: n
snippet: y
---

# Watermarks{#watermarks}

Image Serving implements a simple visual watermarking facility.

A watermark typically is a semi-transparent image, but it may be text, or a more complex, layered composite image. The server will layer the watermark over the reply image after all view attributes ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) have been applied.

Watermarking is enabled by setting `attribute::Watermark` to a valid catalog entry which would contain the watermark image or template. If `attribute::Watermark` is set in a named catalog, the server will add the watermark to all image requests which reference the catalog id in the request URL. If `default::Watermark` is set (in the default catalog, [!DNL default.ini]), the watermark will be applied to all image requests regardless of whether they reference a catalog or not.

Watermarks are not applied to images returned in response to thumbnail requests ( `req=tmb`) and certain requests from Scene7 viewers.

## Scaling and alignment {#section-89ef9e5926ae438abbd8e70332749b76}

When a watermark is specified, the server will first generate the composite image (the *target image*) to which the watermark needs to be applied (before applying the view transforms). The server then generates the composite image for the watermark just like any other image (the *watermark image*).

Unlike standard images, `sizeN=` may be specified for layer=0 or layer=comp of the watermark image. This allows scaling of the watermark image relative to the target image. If `sizeN=` is not specified, the watermark image retains its pixel size when being merged with the target image.

Request commands (such as `fmt=`) and view commands (such as `wid=`) are ignored in watermark records, with the exception of `align=`. `align=` can be used to position the watermark image relative to the watermark image relative to the target image. This allows positioning of the watermark relative to a corner or edge of the target image.

After scaling and aligning, the server will layer the watermark image over the target image using the `blendMode=` and `opac=` values specified for `layer=0` or `layer=comp` of the watermark image. Finally, the request and view commands specified for the target image are applied to construct the reply image.

Note that the watermark image will never extend over any blank space added to the reply image by the `wid=` and `hei=` commands.

## Example {#section-0408c977d7324d4cb0e76a91cdfa2acd}

A typical watermark might consist of a simple RGBA image containing a logo or a copyright notice. We create a record in the image catalog (or the default catalog) with `catalog::Id` set to `watermark` and specify the watermark image file in `catalog::Path`. We want to stretch the watermark to fit the view image (without distorting the watermark) while leaving a little extra margin, and reduce the opacity to 20% of the original watermark, so we set `catalog::Modifier` to `sizeN=0.9,0.9&opac=20`. To activate watermarking, set `attribute::Watermark` to the id of the watermark catalog entry, "watermark" in this example. We might want to experiment with different `blendMode=` choices to achieve different watermarking effects.

## See also {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attribute::Watermark](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b) 
