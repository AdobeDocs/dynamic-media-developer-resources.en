---
description: Default thumbnail size. Used instead of attribute DefaultPix for thumbnail requests (req=tmb).
seo-description: Default thumbnail size. Used instead of attribute DefaultPix for thumbnail requests (req=tmb).
seo-title: DefaultThumbPix
solution: Experience Manager
title: DefaultThumbPix
uuid: 7b310aab-6d38-45f3-a3e7-b074a8e7a795
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# DefaultThumbPix{#defaultthumbpix}

Default thumbnail size. Used instead of attribute::DefaultPix for thumbnail requests (req=tmb).

The server constrains reply images to be no larger than this width and height, if a thumbnail request ( `req=tmb`) does not specify the size explicitly not specify the view size explicitly using `wid=`, `hei=`, or `scl=`.

## Properties {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Two integer numbers, 0 or larger, separated by a comma. Width and height in pixels. Either or both values may be set to 0 to keep them unconstrained.

Does not apply to nested/embedded requests.

## Default {#section-2c4a4f14540449638822913513170ff1}

Inherited from `default::DefaultThumbPix` if not defined or if empty.

## See also {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1) 
