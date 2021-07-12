---
description: Grayscale default color space. Specifies the name of the ICC color profile to be used for grayscale response images when no output color space is specified with icc=.
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
---
# IccProfileGray{#iccprofilegray}

Grayscale default color space. Specifies the name of the ICC color profile to be used for grayscale response images when no output color space is specified with icc=.

## Properties {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this material catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be a grayscale profile.

## Default {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

Inherited from `default::IccProfileGray` if not defined or if empty.

## See also {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
