---
description: RGB default output color profile. Specifies the name of the ICC color profile to be used for RGB response images when no output color space is specified with icc= and for certain RGB color values specified with various Image Rendering commands, such as bgc= and color=.
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
---
# IccProfileRgb{#iccprofilergb}

RGB default output color profile. Specifies the name of the ICC color profile to be used for RGB response images when no output color space is specified with icc= and for certain RGB color values specified with various Image Rendering commands, such as bgc= and color=.

## Properties {#section-b4a1bd92e99047479a5036413525a6d9}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this material catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be an RGB profile.

## Default {#section-5809772f8e96438ab7626d323c66a4ba}

Inherited from `default::IccProfileRgb` if not defined or if empty.

## See also {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
