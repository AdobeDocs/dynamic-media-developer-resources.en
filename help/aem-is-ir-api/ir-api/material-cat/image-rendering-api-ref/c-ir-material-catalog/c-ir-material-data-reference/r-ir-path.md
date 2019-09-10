---
description: Image file path. Relative path and name of a texture or decal image file.
seo-description: Image file path. Relative path and name of a texture or decal image file.
seo-title: Path *
solution: Experience Manager
title: Path *
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e85a358-3f2f-4b8b-a98f-03de2a1a8a4c
index: y
internal: n
snippet: y
---

# Path *{#path}

Image file path. Relative path and name of a texture or decal image file.

The server combines this value with `attribute::RootPath` to build the actual image file path. May also be an absolute path.

Used to specify the texture image file for texture, cabinet, and window covering materials, and the RGB or RGBA image file for decal and wall border materials. Not all cabinet and window covering materials require a separate repeatable texture image.

## Properties {#section-8c12ea24f21d4472be677581893e6681}

Text string. Required for texture and decal materials, optional for cabinet and window covering materials. If specified, it must be a valid relative or absolute file path. Must be empty for solid color materials.

## Supported file formats {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Image Rendering supports the same source image formats as Scene7 Image Serving.

Applications which require image data in multiple different resolutions will perform best when using the Scene7 pyramid TIFF (PTIFF) multi-resolution format. Image Serving includes the Image Converter (IC) utility which creates PTIFF images from any supported format.

Refer to the description of the IC utility in the Image Serving documentation for a complete list of supported file formats.

## Default {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

None.

## See also {#section-1bf37fab8e5f4c42a03b785abafc53bd}

IC Utility, [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) 
