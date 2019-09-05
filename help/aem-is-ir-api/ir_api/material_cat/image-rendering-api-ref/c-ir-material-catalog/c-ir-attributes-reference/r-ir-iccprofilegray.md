---
description: Grayscale default color space. Specifies the name of the ICC color profile to be used for grayscale response images when no output color space is specified with icc=.
seo-description: Grayscale default color space. Specifies the name of the ICC color profile to be used for grayscale response images when no output color space is specified with icc=.
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
topic: Scene7 Image Serving - Image Rendering API
uuid: f3ab6149-62eb-4b1a-827c-faeeba3863a5
index: y
internal: n
snippet: y
---

# IccProfileGray{#iccprofilegray}

Grayscale default color space. Specifies the name of the ICC color profile to be used for grayscale response images when no output color space is specified with icc=.

## Properties {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this material catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be a grayscale profile.

## Default {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

Inherited from `default::IccProfileGray` if not defined or if empty.

## See also {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcGray](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2), [attribute::RootPath](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) 
