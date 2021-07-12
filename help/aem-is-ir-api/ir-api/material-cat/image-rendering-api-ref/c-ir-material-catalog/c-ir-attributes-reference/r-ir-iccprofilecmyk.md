---
description: CMYK default color space. Specifies the name of the ICC color profile to be used for gray-scale response images when no output color space is specified with icc=.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c36ea45d-dc91-4afa-825a-7af49738101c
---
# IccProfileCmyk{#iccprofilecmyk}

CMYK default color space. Specifies the name of the ICC color profile to be used for gray-scale response images when no output color space is specified with icc=.

## Properties {#section-849678b272954bdcb236f49aa54f1609}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this image catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be a CMYK profile.

## Default {#section-55026b7454af4d868bcb47f7743c9c5b}

Inherited from `default::IccProfileCmyk` if not defined or if empty.

## See also {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
