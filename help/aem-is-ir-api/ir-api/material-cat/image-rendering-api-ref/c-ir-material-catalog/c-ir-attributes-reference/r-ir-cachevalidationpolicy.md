---
title: CacheValidationPolicy
description: Server cache validation policy. Specifies when server-side cache entries are validated.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
TQID: 'https://experienceleague.adobe.com/8WipxBM2HngJP5f8LOJmFPA5jZTyJt6Q5P9mZnzDPsY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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
