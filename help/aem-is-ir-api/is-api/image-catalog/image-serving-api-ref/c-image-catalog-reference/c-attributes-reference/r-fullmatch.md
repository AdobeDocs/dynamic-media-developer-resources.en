---
description: Catalog matching option.
seo-description: Catalog matching option.
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
topic: Scene7 Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
index: y
internal: n
snippet: y
---

# FullMatch{#fullmatch}

Catalog matching option.

A catalog entry is specified as a ` *`rootId`*/ *`imageId`*` pair in HTTP requests. When parsing, a catalog is selected if ` *`rootId`*` matches the `attribute::RootId` value of the catalog, and the catalog record is identified by matching ` *`imageId`*` with a `catalog::Id` value. If a catalog is found, but there is no catalog entry matching ` *`imageId`*`, the server can do one of two things:

If `attribute::FullMatch` is not set, the server uses the attributes of the matched catalog. In this case, ` *`rootId`*` is replaced by `attribute::RootPath` (or `default::RootPath`, if not specified in this catalog).

If `attribute::FullMatch` is set, the server completely ignores the catalog, as if no catalog had been matched, and proceed using default catalog attributes. In this case, ` *`rootId`*` remains part of the path (which is prepended by `default::RootPath`).

## Properties {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Flag. Set to 0 for default behavior or to 1 to enable full-match behavior.

## Default {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Inherited from `default::FullMatch` if not defined or if empty.

## See also {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](r_id_cat.md#reference_C3F3CE9AAAC4451796A846D6722383E5) 
