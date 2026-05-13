---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36660bb-d2ec-464c-b578-fe862bca5c50
TQID: 'https://experienceleague.adobe.com/n-LXS-OEhuBOkse44eQ0HTHV-Bx5BRH3AjgE0xInqK8'
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
# TimeStamp{#timestamp}

If `attribute::UseLastModified` is set, the `catalog::TimeStamp` value is returned in the HTTP response as a Last-Modified HTTP header. The Last-Modified header is always returned for static contents, even if `attribute::UseLastModified` is not set.

For image and SVG contents, `catalog::TimeStamp` is also used for catalog-based cache validation (see [attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Properties {#section-2298a384b5cb43929542655c5a49beb2}

Date/time value in Java format. Can be either the integer number of milliseconds since midnight, January 1, 1970 UTC/GMT, or a date/time string value with one of the following formats:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* is in the range 0 - 23.

*`zzz`* is a three or four character time zone code such as 'GMT' or 'PST'. Account for Daylight Savings Time in the time zone code. For example, 'PST' for Pacific Standard Time, versus 'PDT' for Pacific Daylight Savings Time).

*`offset`* is a time zone offset in hours or `hours:minutes`, relative to GMT. For example, 'PDT' is equivalent to 'GMT -7'.

All elements of string formatted date/time values must be present. If the date/time value is not formatted correctly it is ignored and the modification time of the `*`catalog`*.ini` file is used instead.

## Default {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` if the field is empty or not present.

## See also {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
