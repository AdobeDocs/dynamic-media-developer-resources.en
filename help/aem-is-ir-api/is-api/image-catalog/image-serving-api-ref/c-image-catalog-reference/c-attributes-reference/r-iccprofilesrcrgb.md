---
description: RGB default input color profile. Specifies the name of the ICC color profile to be used for RGB source images which do not embed a color profile and for certain RGB color values specified with various Image Serving commands, such as color=.
seo-description: RGB default input color profile. Specifies the name of the ICC color profile to be used for RGB source images which do not embed a color profile and for certain RGB color values specified with various Image Serving commands, such as color=.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
---

# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB default input color profile. Specifies the name of the ICC color profile to be used for RGB source images which do not embed a color profile and for certain RGB color values specified with various Image Serving commands, such as color=.

## Properties {#section-3cd753196959462e9e674dab0b033d08}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this image catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be an RGB profile.

## Default {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Inherited from `default::IccProfileSrcRgb` if not defined or if empty. If `attribute::IccProfileSrcRgb` does not resolve to a valid profile, `attribute::IccProfileRgb` is used instead.

## See also {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) 
