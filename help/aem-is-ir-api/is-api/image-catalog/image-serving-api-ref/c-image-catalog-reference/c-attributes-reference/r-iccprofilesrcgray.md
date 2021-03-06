---
description: Grayscale default input color profile. Specifies the name of the ICC color profile to be used for grayscale source images which do not embed a color profile and for certain grayscale color values specified with various Image Serving commands, such as color=.
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54290f71-36b2-4b37-ac04-4fe85c1f34ab
---
# IccProfileSrcGray{#iccprofilesrcgray}

Grayscale default input color profile. Specifies the name of the ICC color profile to be used for grayscale source images which do not embed a color profile and for certain grayscale color values specified with various Image Serving commands, such as color=.

## Properties {#section-8cbb316df6eb463aaca7b308d3568086}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this image catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be a grayscale profile.

## Default {#section-bcc7250715884412bd0780f60d1cce7b}

Inherited from `default::IccProfileSrcGray` if not defined or if empty. If `attribute::IccProfileSrcGray` does not resolve to a valid profile, `attribute::IccProfileGray` is used instead.

## See also {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
