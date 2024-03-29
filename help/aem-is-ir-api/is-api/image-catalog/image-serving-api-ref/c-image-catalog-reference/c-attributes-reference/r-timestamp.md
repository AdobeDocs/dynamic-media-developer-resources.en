---
title: TimeStamp
description: Default image modification time stamp. It provides a default value for catalog TimeStamp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
---
# TimeStamp{#timestamp}

Default image modification time stamp. Provides a default value for catalog::TimeStamp.

 If not specified, the server uses the modification date/time of this [!DNL *`catalog`*.ini] file.

## Properties {#section-647066e62ce44a84b627fdd0b2f7cfec}

Date/time value. It can be either the integer number of milliseconds since midnight, January 1, 1970 UTC/GMT, or a date/time string value with one of the following formats:

The date/time value *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

The date/time value *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

The time value *`hh`* is in the range 0&ndash;23.

The time value *`zzz`* is a three or four character time zone code such as `GMT` or `PST`. Daylight savings time must be accounted for in the time zone code (for example, `PST` for Pacific Standard Time, vs `PDT` for Pacific Daylight Savings Time).

The time value *`offset`* is a time zone offset in hours or hours:minutes, relative to GMT. For example, `PDT` is equivalent to `GMT -7`.

All elements of string-formatted date/time values must be present. If the date/time value is not formatted correctly, it is ignored and the modification time of the [!DNL *`catalog`*.ini] file is used instead.

## Default {#section-ac465313c97943ed97d41ea852329177}

If empty or not defined, the server uses the file modification time of this `*`catalog`*.ini` file.

## See also {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
