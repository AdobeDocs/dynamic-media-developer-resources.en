---
description: Server cache validation policy. Specifies when server-side cache entries are validated.
seo-description: Server cache validation policy. Specifies when server-side cache entries are validated.
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Scene7 Image Serving - Image Rendering API
uuid: 48c4f39c-3baf-4c54-b5dd-44fa4bc713f2
index: y
internal: n
snippet: y
---

# CacheValidationPolicy{#cachevalidationpolicy}

Server cache validation policy. Specifies when server-side cache entries are validated.

With expiration-based validation, source images are periodically checked whether they have changed. With catalog-based validation, source images are checked only after the `catalog::TimeStamp` value changed.

Catalog-based validation is recommended when image catalogs are used. Expiration-based validation should be used when images are referenced directly, without the use of an image catalog.

## Properties {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 to select expiration-based validation, 1 to select catalog-based cache validation.

## Default {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Inherited from `default::CacheValidationPolicy` if not defined or if empty.

## See also {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog::TimeStamp](../../../../../is_api/image_catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded) 
