---
description: Grayscale default output color profile. Specifies the name of the ICC color profile to be used for grayscale response images when no output color space is specified with icc= and for certain grayscale color values specified with various Image Serving commands, such as color=.
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
---
# IccProfileGray{#iccprofilegray}

Grayscale default output color profile. Specifies the name of the ICC color profile to be used for grayscale response images when no output color space is specified with icc= and for certain grayscale color values specified with various Image Serving commands, such as color=.

## Properties {#section-03f090ee2acf4537b83f78840d23ecab}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this image catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be a grayscale profile.

## Default {#section-95ba3ab15edc4259b657c6ebf8783d61}

Inherited from `default::IccProfileGray` if not defined or if empty.

## See also {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
