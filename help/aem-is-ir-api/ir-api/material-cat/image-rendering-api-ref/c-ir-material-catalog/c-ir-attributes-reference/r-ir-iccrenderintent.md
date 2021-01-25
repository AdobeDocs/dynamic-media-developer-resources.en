---
description: Color conversion rendering intent. Provides the default rendering intent for color conversions when the render intent is not specified with icc=.
seo-description: Color conversion rendering intent. Provides the default rendering intent for color conversions when the render intent is not specified with icc=.
seo-title: IccRenderIntent
solution: Experience Manager
title: IccRenderIntent
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a9648405-32c3-4762-bbb2-11e97d4f8374
---

# IccRenderIntent{#iccrenderintent}

Color conversion rendering intent. Provides the default rendering intent for color conversions when the render intent is not specified with icc=.

## Properties {#section-0a38c60e1525426185616c42824aee2c}

Enum. Set to 0 for perceptual, 1 for relative colorimetric, 2 for saturation, 3 for absolute colorimetric. Keep empty or set to any other value to use the default rendering intent defined in the color profile.

## Default {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Inherited from `default::IccRenderIntent`if not defined. If empty, 'relative colorimetric' is applied.

## See also {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) 
