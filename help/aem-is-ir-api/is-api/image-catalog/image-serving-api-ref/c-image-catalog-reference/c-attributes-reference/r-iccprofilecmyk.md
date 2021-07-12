---
description: CMYK default output color profile. Specifies the name of the ICC color profile to be used for CMYK response images when no output color space is specified with icc= and for certain CMYK color values specified with various Image Serving commands, such as color=.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
---
# IccProfileCmyk{#iccprofilecmyk}

CMYK default output color profile. Specifies the name of the ICC color profile to be used for CMYK response images when no output color space is specified with icc= and for certain CMYK color values specified with various Image Serving commands, such as color=.

## Properties {#section-d8b6102cc1c744d482f99808ccfcaa24}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this image catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be a CMYK profile.

## Default {#section-62442df09a724950bfbdd0640b3e6678}

Inherited from `default::IccProfileCmyk` if not defined or if empty.

## See also {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
