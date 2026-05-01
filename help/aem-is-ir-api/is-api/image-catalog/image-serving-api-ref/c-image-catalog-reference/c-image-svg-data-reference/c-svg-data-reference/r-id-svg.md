---
title: Id
description: Typically, a short and unique identifier, such as a SKU number, possibly with some sort of suffix, such as if a SKU has multiple images or has locale-specific variations.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d7b37180-cc93-41cd-bf14-5c262b046fbc
TQID: https://experienceleague.adobe.com/pV-mlwi-KP1OGg443FKeh2ae4D1jNykzM3-O-4UOC9I
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
# Id{#id}

Typically, a short and unique identifier, such as a SKU number, possibly with some sort of suffix, such as if a SKU has multiple images or has locale-specific variations. May also be a more complex string which looks more like a file path, to support easy retrofitting of web sites with Image Serving.

>[!NOTE]
>
>The image and SVG tables are merged into a single table when the image catalog is loaded. Id values must be unique across both tables. The SVG record is discarded if the image table contains a record with the same ID value. Static content is managed with a separate table; static content items and image/SVG items may thus have the same Id values.

## Properties {#section-874a6853f67b4b229341ca76682884ae}

Text string. Required. Record identifier for the image/SVG or static content data table. Each `catalog::Id` value within this image catalog/SVG catalog or within this static content catalog must be unique and must not include ',' characters.

## Default {#section-a26e7d83a5ee44b5918baef82ee48e14}

None.

## See also {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
