---
description: Static content catalog data file paths. Specifies the files that contain the static content data for this catalog.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
---
# StaticContentCatalogFile{#staticcontentcatalogfile}

Static content catalog data file paths. Specifies the files that contain the static content data for this catalog.

Static content catalog data files are loaded in the order specified. If the same `static::Id` value occurs in more than one record (either in the same or different catalog files), the last instance prevails.

## Properties {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

One or more text string values, separated by commas. Optional. Each value must be an absolute file path or path relative to the catalog folder.

## Default {#section-702edfbc00c54fc29e412a3ff99fef2b}

Empty, which indicates that this image catalog does not include any static content data.

## See also {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Catalog Data](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
