---
description: RGB default output color profile. Specifies the name of the ICC color profile to be used for RGB response images when no output color space is specified with icc= and for certain RGB color values specified with various Image Serving commands, such as color=.
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
---
# IccProfileRgb{#iccprofilergb}

RGB default output color profile. Specifies the name of the ICC color profile to be used for RGB response images when no output color space is specified with icc= and for certain RGB color values specified with various Image Serving commands, such as color=.

## Properties {#section-3dd55c954d4d4ad4bb715ed7cee31025}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this image catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be an RGB profile.

## Default {#section-dfe08dd7b851453ca816623a4179955b}

Inherited from `default::IccProfileRgb` if not defined or if empty.

## See also {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
