---
title: IccProfileSrcCmyk
description: CMYK default input color profile. Specifies the name of the ICC color profile to be used for CMYK source images which do not embed a color profile and for certain CMYK color values specified with various Image Serving commands, such as color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
---
# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK default input color profile. Specifies the name of the ICC color profile to be used for CMYK source images which do not embed a color profile and for certain CMYK color values specified with various Image Serving commands, such as color=.

## Properties {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this image catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be a CMYK profile.

## Default {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Inherited from `default::IccProfileSrcCmyk` if not defined or if empty. If `attribute::IccProfileSrcCmyk` does not resolve to a valid profile, `attribute::IccProfileCmyk` is used instead.

## See also {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
