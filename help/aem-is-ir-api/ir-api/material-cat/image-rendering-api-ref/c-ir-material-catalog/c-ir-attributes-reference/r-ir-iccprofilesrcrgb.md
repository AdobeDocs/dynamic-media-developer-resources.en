---
title: IccProfileSrcRgb
description: RGB default input color profile. Specifies the name of the ICC color profile to be used for RGB material images and vignettes which do not embed a color profile. Also for RGB color values specified with various Image Rendering commands, such as bgc= and color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
---
# IccProfileSrcRgb{#iccprofilesrcrgb}

RGB default input color profile. Specifies the name of the ICC color profile to be used for RGB material images and vignettes which do not embed a color profile. Also for RGB color values specified with various Image Rendering commands, such as `bgc=` and `color=`.

## Properties {#section-c22966bba03e43c08e9d3fb91bfdd465}

Text string. If specified, must be a valid `icc::Name` value from the ICC profile map of either this image catalog or the default catalog, or a file path relative to `attribute::RootPath`. The referenced ICC profile must be an RGB profile.

## Default {#section-0171cd6680284bfa9844b9cc3644ca61}

Inherited from `default::IccProfileSrcRgb` if not defined or if empty. If `attribute::IccProfileSrcRgb` does not resolve to a valid profile, `attribute::IccProfileRgb` is used instead.

## See also {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
