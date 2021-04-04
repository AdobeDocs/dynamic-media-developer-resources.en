---
description: Default thumbnail resolution. Provides a default for the thumbnail object resolution in case a particular catalog record does not contain a valid catalog ThumbRes value.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
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
