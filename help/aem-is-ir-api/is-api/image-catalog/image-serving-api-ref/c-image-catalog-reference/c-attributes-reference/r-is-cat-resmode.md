---
title: ResMode
description: Default resampling mode. Specifies the default resampling and interpolation attributes to be used for scaling image data.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
---
# ResMode{#resmode}

Default resampling mode. Specifies the default resampling and interpolation attributes to be used for scaling image data.

 Used when `resMode=` is not specified in a request.

## Properties {#section-493f900be522486f97710cebdc4460c2}

Enum. Set to 2 for `bilin`, 3 for `bicub`, or 4 for `sharp2` interpolation mode (see [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) for details). `sharp` (1) is being deprecated. Use `sharp2` (4) instead for best results.

## Default {#section-35f980e745fc4d79a2621e8abacc724d}

Inherited from `default::ResMode` if not defined or if empty.

## See also {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
