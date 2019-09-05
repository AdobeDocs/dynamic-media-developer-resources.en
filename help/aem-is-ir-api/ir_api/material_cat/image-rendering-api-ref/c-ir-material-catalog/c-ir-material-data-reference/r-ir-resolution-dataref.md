---
description: Resolution. "Real-world" image resolution, typically expressed as pixels per inch, but may also be in other units, such as pixels per meter.
seo-description: Resolution. "Real-world" image resolution, typically expressed as pixels per inch, but may also be in other units, such as pixels per meter.
seo-title: Resolution
solution: Experience Manager
title: Resolution
topic: Scene7 Image Serving - Image Rendering API
uuid: ec554522-169b-4c71-af3b-b8e3c6ca3bb0
index: y
internal: n
snippet: y
---

# Resolution{#resolution}

Resolution. "Real-world" image resolution, typically expressed as pixels per inch, but may also be in other units, such as pixels per meter.

## Properties {#section-985ca2ad858c4e9c9cbb303f55447553}

Real number, larger than 0. Required for texture and decal materials, unless the image resolution is the same as attribute::Resolution. Ignored by solid color and cabinet materials.

## Default {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` is used if the field is not present, if the value is 0 or negative, or if the field is empty.

## See also {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) , [res=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04) 
