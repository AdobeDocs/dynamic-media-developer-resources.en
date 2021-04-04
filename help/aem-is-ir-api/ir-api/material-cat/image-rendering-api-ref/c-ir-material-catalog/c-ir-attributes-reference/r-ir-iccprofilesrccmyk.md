---
description: CMYK default input color profile. Specifies the name of the ICC color profile to be used for CMYK material images which do not embed a color profile.
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
---
# IccProfileSrcCmyk{#iccprofilesrccmyk}

CMYK default input color profile. Specifies the name of the ICC color profile to be used for CMYK material images which do not embed a color profile.

## Properties {#section-0cee77438d914c319ec876edb3490821}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this image catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be a CMYK profile.

## Default {#section-11f6239e0dd14827abf4a95c1b30161c}

Inherited from `default::IccProfileSrcCmyk` if not defined or if empty. If `attribute::IccProfileSrcCmyk` does not resolve to a valid profile, `attribute::IccProfileCmyk` will be used instead.

## See also {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
