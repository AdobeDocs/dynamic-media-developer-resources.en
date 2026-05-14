---
title: CacheValidationPolicy
description: Server cache validation policy. Specifies when server-side cache entries are validated.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
TQID: 'https://experienceleague.adobe.com/s7dYUadAD1i1ROqCafEZOa5Tztl3ss2HAXnEsPiRGr8'
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

With expiration-based validation, source images are periodically checked whether they have changed. With catalog-based validation, source images are checked only after the `catalog::TimeStamp` value changed.

Catalog-based validation is recommended when image catalogs are used. Expiration-based validation should be used when images are referenced directly, without the use of an image catalog.

## Properties {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 to select expiration-based validation, 1 to select catalog-based cache validation.

## Default {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Inherited from `default::CacheValidationPolicy` if not defined or if empty.

## See also {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
