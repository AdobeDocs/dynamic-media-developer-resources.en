---
description: Image data file paths. Specifies the files that contain the image data for this catalog.
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
TQID: 'https://experienceleague.adobe.com/MhxEBtyw3JIvMg5miQotPPCeoLeWATtXy0fbRtE7ePs'
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
# CatalogFile{#catalogfile}

Image data file paths. Specifies the files that contain the image data for this catalog.

Image data files are loaded in the order specified. If the same `catalog::Id` value occurs in more than one record (either in the same or different catalog files), the last instance prevails.

## Properties {#section-6da55f145ecd4e31a5de52637a436983}

One or more text string values, separated by commas. Optional. Each value must be an absolute file path or path relative to the catalog folder.

## Default {#section-80f91cd7a6b2479ebb310319e9c74da7}

Empty, which indicates that this image catalog does not include any image data.

## See also {#section-910b67c5041d44d99a105ad43ff63a37}

[Catalog Data Fields](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
