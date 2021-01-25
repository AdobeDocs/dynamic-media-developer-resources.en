---
description: Image anchor. Specifies the anchor point (hotspot) of a repeatable texture, wall border, or decal image.
seo-description: Image anchor. Specifies the anchor point (hotspot) of a repeatable texture, wall border, or decal image.
seo-title: Anchor
solution: Experience Manager
title: Anchor
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0b1a0fea-b299-44dc-b9fd-5916130b2ef3
---

# Anchor{#anchor}

Image anchor. Specifies the anchor point (hotspot) of a repeatable texture, wall border, or decal image.

 A repeatable texture is applied to a vignette object so that the texture anchor point is located at the object's texture origin point. A decal image is applied to a vignette object so that the decal anchor point is located at the object's decal origin point. For wall borders, only the x value is used; the y value is ignored.

## Properties {#section-bc4bc8b897c64535b88681e57d72942f}

Two integer numbers, separated by a comma. Pixel offset relative to the top, left corner of the image. Ignored if `catalog::Alignment=3` and by solid color and cabinet materials.

## Default {#section-b7ccc419a356415294706cd295ae96c9}

If the field is empty or not present, the top-left corner (0,0) of the image for repeatable texture materials is used, or the center of the image in case of decal materials.

## See also {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26) 
