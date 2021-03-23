---
description: Embed Color Profile. Specifies whether the working ICC color profile or the profile specified with icc= should be embedded in the reply image.
solution: Experience Manager
title: iccEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# iccEmbed{#iccembed}

Embed Color Profile. Specifies whether the working ICC color profile or the profile specified with icc= should be embedded in the reply image.

 `iccEmbed=0|1`

## Properties {#section-e36aa3c63a974b969d9e4f43fe5a37ab}

Request attribute. Ignored if no profile is available for embedding.

## Default {#section-01948f6cd7a2415091004cd7526436c7}

`iccEmbed=0`, for no embedding of ICC profiles in output images. Ignored if the output image format does not support embedding of ICC profiles.

See [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) for details.

## See also {#section-2105c6441d2b42edb15c7abc4e20d7fc}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) , [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) 
