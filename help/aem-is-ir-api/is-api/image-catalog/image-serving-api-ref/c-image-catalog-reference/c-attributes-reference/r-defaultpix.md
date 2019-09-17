---
description: Default view size.
seo-description: Default view size.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Scene7 Image Serving - Image Rendering API
uuid: f5d2e4f7-f9c5-40a5-8a64-67241fcb0242
---

# DefaultPix{#defaultpix}

Default view size.

The server constrains reply images to be no larger than this width and height, if the request does not specify the view size explicitly using `wid=`, `hei=`, or `scl=`.

## Properties {#section-c3e658cf82c540d986b118f74f0fe1b2}

Two integer numbers, 0 or larger, separated by a comma. Width and height in pixels. Either or both values may be set to 0 to keep them unconstrained.

Does not apply to nested/embedded requests.

## Default {#section-b7338b2bf5114fff83b0714a57b20639}

Inherited from `default::DefaultPix` if not defined or if empty.

## See also {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [catalog::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5) 
