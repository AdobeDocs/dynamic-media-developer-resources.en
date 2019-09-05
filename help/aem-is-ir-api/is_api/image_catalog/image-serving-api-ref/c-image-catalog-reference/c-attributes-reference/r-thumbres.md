---
description: Default thumbnail resolution. Provides a default for the thumbnail object resolution in case a particular catalog record does not contain a valid catalog ThumbRes value.
seo-description: Default thumbnail resolution. Provides a default for the thumbnail object resolution in case a particular catalog record does not contain a valid catalog ThumbRes value.
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
topic: Scene7 Image Serving - Image Rendering API
uuid: 90b50953-9d33-4cbc-95ef-762812ac8764
index: y
internal: n
snippet: y
---

# ThumbRes{#thumbres}

Default thumbnail resolution. Provides a default for the thumbnail object resolution in case a particular catalog record does not contain a valid catalog::ThumbRes value.

Used only for thumbnail requests ( `req=tmb`) and when `catalog::ThumbType=3`.

## Properties {#section-88d37d0e030f4879a9e584dd2cc780f3}

Real number, larger than 0.Typically expressed as pixels per inch, but may also be in other units, such as pixels per meter.

## Default {#section-86588899ec9b4276a98b03d7faf64003}

Inherited from `default::ThumbRes` if not defined or if empty.

## See also {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalog::ThumbRes](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69) 
