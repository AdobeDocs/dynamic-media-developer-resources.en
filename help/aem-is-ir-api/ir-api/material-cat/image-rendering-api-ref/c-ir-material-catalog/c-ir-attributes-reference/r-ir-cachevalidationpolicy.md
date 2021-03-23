---
description: Server cache validation policy. Specifies when server-side cache entries are validated.


solution: Experience Manager
title: CacheValidationPolicy

feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# CacheValidationPolicy{#cachevalidationpolicy}

Server cache validation policy. Specifies when server-side cache entries are validated.

With expiration-based validation, source materials and vignettes are periodically checked to see whether they have changed. With catalog-based validation, source images are checked only after the `catalog::TimeStamp` value changed.

Catalog-based validation is recommended when both material and vignette catalogs are used. Expiration-based validation should be used when vignettes are referenced in Image Rendering requests directly by path.

## Properties {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 to select expiration-based validation. 1 to select catalog-based cache validation.

## Default {#section-e09f3af8b6b3497d963199988dc5345d}

Inherited from `default::CacheValidationPolicy` if not defined or if empty.

## See also {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) 
