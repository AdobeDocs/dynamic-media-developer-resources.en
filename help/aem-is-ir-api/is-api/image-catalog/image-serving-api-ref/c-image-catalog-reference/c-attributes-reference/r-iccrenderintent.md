---
title: IccRenderIntent
description: Color conversion rendering intent. It provides the default rendering intent for color conversions when `icc=` is not specified for the render intent.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
---
# IccRenderIntent{#iccrenderintent}

Color conversion rendering intent. Provides the default rendering intent for color conversions when the render intent is not specified with `icc=`.

## Properties {#section-2540099fb2fc47d29b04642da4f5922a}

Enum. Set to 0 for perceptual, 1 for relative colorimetric, 2 for saturation, 3 for absolute colorimetric.

## Default {#section-61a05067905b44099c228e15de279dbd}

Inherited from `default::IccRenderIntent` if not defined or if empty.

## See also {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;, [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
