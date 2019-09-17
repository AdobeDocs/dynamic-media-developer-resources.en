---
description: Default resampling mode. Specifies the default resampling and interpolation attributes to be used for scaling image data.
seo-description: Default resampling mode. Specifies the default resampling and interpolation attributes to be used for scaling image data.
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
---

# ResMode{#resmode}

Default resampling mode. Specifies the default resampling and interpolation attributes to be used for scaling image data.

 Used when `resMode=` is not specified in a request.

## Properties {#section-493f900be522486f97710cebdc4460c2}

Enum. Set to 2 for `bilin`, 3 for `bicub`, or 4 for `sharp2` interpolation mode (see ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` for details). `sharp` (1) is being deprecated. Use `sharp2` (4) instead for best results.

## Default {#section-35f980e745fc4d79a2621e8abacc724d}

Inherited from `default::ResMode` if not defined or if empty.

## See also {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2) 
