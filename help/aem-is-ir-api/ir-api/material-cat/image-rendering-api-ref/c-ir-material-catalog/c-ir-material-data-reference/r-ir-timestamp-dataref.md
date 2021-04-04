---
description: File modification time stamp. Specifies the date/time the image and/or data files attached to this catalog record were last modified.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
---
# TimeStamp{#timestamp}

File modification time stamp. Specifies the date/time the image and/or data files attached to this catalog record were last modified.

If `attribute::UseLastModified` is set, the most recent of the `catalog::TimeStamp` and `vignette::TimeStamp` values of all materials and the vignette involved in the request is returned in the HTTP response as a last-modified header.

>[!NOTE]
>
>The actual file times of the image or data files attached to this catalog record are never used for this purpose.

`catalog::TimeStamp` is also used for catalog-based cache validation (see ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Properties {#section-42f09e375e72492b87a3a486da7df808}

Date/time value in Java format. Can be either the integer number of milliseconds since midnight, January 1, 1970 UTC/GMT or a date/time string value with one of the following formats:

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* is in the range 0 to 23. 
* *[!DNL zzz]* is a 3 or 4 character time zone code such as 'GMT' or 'PST'. Daylight Savings Time must be accounted for in the time zone code (for example, 'PST' for Pacific Standard Time, versus 'PDT' for Pacific Daylight Savings Time). 
* *[!DNL offset]* is a time zone offset in hours or hours:minutes, relative to GMT. For example, 'PDT' is equivalent to 'GMT -7'.

All elements of string formatted date/time values must be present. If the date/time value is not formatted correctly it is ignored and the modification time of the *catalog*.ini file is used instead.

## Default {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` is the field is empty or not present.

## See also {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
