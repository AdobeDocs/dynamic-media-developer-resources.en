---
description: Resolution. "Real-world" image resolution, typically expressed as pixels per inch, but may also be in other units, such as pixels per meter.
solution: Experience Manager
title: Resolution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
---
# Resolution{#resolution}

Resolution. "Real-world" image resolution, typically expressed as pixels per inch, but may also be in other units, such as pixels per meter.

## Properties {#section-985ca2ad858c4e9c9cbb303f55447553}

Real number, larger than 0. Required for texture and decal materials, unless the image resolution is the same as attribute::Resolution. Ignored by solid color and cabinet materials.

## Default {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` is used if the field is not present, if the value is 0 or negative, or if the field is empty.

## See also {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) , [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
