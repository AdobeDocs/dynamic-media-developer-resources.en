---
description: Catalog matching option.
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
TQID: 'https://experienceleague.adobe.com/5eTvORUSVsXHReAaiVMGSizooDQ9Wq--dXrBo0c9C7c'
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
# FullMatch{#fullmatch}

Catalog matching option.

A catalog entry is specified as a `*`rootId`*/ *`imageId`*` pair in HTTP requests. When parsing, a catalog is selected if `*`rootId`*` matches the `attribute::RootId` value of the catalog, and the catalog record is identified by matching `*`imageId`*` with a `catalog::Id` value. If a catalog is found, but there is no catalog entry matching `*`imageId`*`, the server can do one of two things:

If `attribute::FullMatch` is not set, the server uses the attributes of the matched catalog. In this case, `*`rootId`*` is replaced by `attribute::RootPath` (or `default::RootPath`, if not specified in this catalog).

If `attribute::FullMatch` is set, the server completely ignores the catalog, as if no catalog had been matched, and proceed using default catalog attributes. In this case, `*`rootId`*` remains part of the path (which is prepended by `default::RootPath`).

## Properties {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Flag. Set to 0 for default behavior or to 1 to enable full-match behavior.

## Default {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Inherited from `default::FullMatch` if not defined or if empty.

## See also {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
