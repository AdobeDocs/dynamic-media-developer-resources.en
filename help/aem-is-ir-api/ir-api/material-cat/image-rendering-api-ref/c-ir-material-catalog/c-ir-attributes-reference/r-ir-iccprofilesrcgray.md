---
description: Grayscale default input color profile. Specifies the name of the ICC color profile to be used for grayscale material images which do not embed a color profile.
seo-description: Grayscale default input color profile. Specifies the name of the ICC color profile to be used for grayscale material images which do not embed a color profile.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e05d1185-ffd6-4c04-a2b8-52228beae37d
---

# IccProfileSrcGray{#iccprofilesrcgray}

Grayscale default input color profile. Specifies the name of the ICC color profile to be used for grayscale material images which do not embed a color profile.

## Properties {#section-97923d8561b845309442d57d017d91a4}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this image catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be a grayscale profile.

## Default {#section-02c52805ee13483dba7878aeab51f889}

Inherited from `default::IccProfileSrcGray` if not defined or if empty. If `attribute::IccProfileSrcGray` does not resolve to a valid profile, `attribute::IccProfileGray` will be used instead.

## See also {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) 
