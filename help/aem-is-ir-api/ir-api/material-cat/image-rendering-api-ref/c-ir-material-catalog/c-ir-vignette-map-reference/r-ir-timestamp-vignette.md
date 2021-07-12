---
description: Modification time stamp. Specifies the date/time this vignette was last modified.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
---
# TimeStamp{#timestamp}

Modification time stamp. Specifies the date/time this vignette was last modified.

If `attribute::UseLastModified` is set, the most recent `vignette::TimeStamp` and `catalog::TimeStamp`value of the vignette and all materials involved in the request is returned in the HTTP response as a last-modified header.

>[!NOTE]
>
>The actual file time of the vignette file is never used for this purpose.

`catalog::TimeStamp` is also used for catalog-based cache validation (see ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Properties {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Date/time value in Java format. Can be either the integer number of milliseconds since midnight, January 1, 1970 UTC/GMT or a date/time string value with one of the following formats:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* is in the range 0 to 23. 
* *[!DNL zzz]* is a 3 or 4 character time zone code such as 'GMT' or 'PST'. Daylight Savings Time must be accounted for in the time zone code (for example, 'PST' for Pacific Standard Time, versus 'PDT' for Pacific Daylight Savings Time). 
* *[!DNL offset]* is a time zone offset in hours or hours:minutes, relative to GMT. For example, 'PDT' is equivalent to 'GMT -7'.

All elements of string formatted date/time values must be present. If the date/time value is not formatted correctly it is ignored and the modification time of the [!DNL *[!DNL catalog]*.ini] file will be used instead.

## Default {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` is the field is empty or not present.

## See also {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
