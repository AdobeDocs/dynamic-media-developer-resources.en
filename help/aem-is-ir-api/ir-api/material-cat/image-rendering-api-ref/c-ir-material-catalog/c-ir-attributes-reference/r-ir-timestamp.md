---
title: TimeStamp
description: Default modification time stamp. Provides a default value for catalog TimeStamp and vignette TimeStamp. If not specified, the server uses the modification date/time of this catalog.ini file.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
---
# TimeStamp{#timestamp}

Default modification time stamp. Provides a default value for `catalog::TimeStamp` and `vignette::TimeStamp`. If not specified, the server uses the modification date/time of this catalog.ini file.

## Properties {#section-910e2562b41c47b78ee6216deeabbbd5}

Date/time value in Java™ format. Can be either the integer number of milliseconds since midnight, January 1, 1970 UTC/GMT, or a date/time string value with one of the following formats:

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]* 

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* is in the range 0 – 23.

*[!DNL zzz]* is a three or four character time zone code such as 'GMT' or 'PST'. Daylight Savings Time must be accounted for in the time zone code (for example, 'PST' for Pacific Standard Time, versus 'PDT' for Pacific Daylight Savings Time).

*[!DNL offset]* is a time zone offset in hours or hours:minutes, relative to GMT. For example, 'PDT' is equivalent to 'GMT -7'.

All elements of string-formatted date/time values must be present. If the date/time value is not formatted correctly, it is ignored and the modification time of the [!DNL *[!DNL catalog]*.ini] file is used instead.

## Default {#section-65fb29a9ea2044df8cb9fe295eb14872}

If empty or not defined, the server uses the file modification time of this [!DNL *[!DNL catalog]*.ini] file.

## See also {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
