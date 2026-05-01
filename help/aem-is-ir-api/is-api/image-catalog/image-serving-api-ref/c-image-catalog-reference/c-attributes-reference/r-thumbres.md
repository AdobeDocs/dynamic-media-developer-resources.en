---
description: Default thumbnail resolution. Provides a default for the thumbnail object resolution in case a particular catalog record does not contain a valid catalog ThumbRes value.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
TQID: https://experienceleague.adobe.com/gQLqvBVHSroLmS5XX7U-AJivW6-Qf9R4z2-NHxl3V0s
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
# ThumbRes{#thumbres}

Default thumbnail resolution. Provides a default for the thumbnail object resolution in case a particular catalog record does not contain a valid catalog::ThumbRes value.

Used only for thumbnail requests ( `req=tmb`) and when `catalog::ThumbType=3`.

## Properties {#section-88d37d0e030f4879a9e584dd2cc780f3}

Real number, larger than 0.Typically expressed as pixels per inch, but may also be in other units, such as pixels per meter.

## Default {#section-86588899ec9b4276a98b03d7faf64003}

Inherited from `default::ThumbRes` if not defined or if empty.

## See also {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalog::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
