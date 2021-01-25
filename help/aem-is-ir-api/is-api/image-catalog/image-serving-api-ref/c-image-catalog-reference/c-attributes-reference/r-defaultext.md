---
description: Default image file suffix. Appended to the catalog Path (or catalog MaskPath) field value if the path does not include a file suffix
seo-description: Default image file suffix. Appended to the catalog Path (or catalog MaskPath) field value if the path does not include a file suffix
seo-title: DefaultExt
solution: Experience Manager
title: DefaultExt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: aa245d18-15cc-41cb-a49d-757d74fe6231
---

# DefaultExt{#defaultext}

Default image file suffix. Appended to the catalog::Path (or catalog::MaskPath) field value if the path does not include a file suffix

A file suffix consists of a period and one or more characters between the period and the end of the string. The suffix is appended to the http path, if the path does not resolve to a catalog entry, and if the last path element does not include a file suffix.

## Properties {#section-b024e6450b414ccc8b83a48a3b4e00f9}

Text string. Must include a leading '.' and one or more characters.

## Default {#section-1194c36ffe0748c5b9ff7d732a506588}

Inherited from `default::DefaultExt` if not defined. If defined but empty, no default suffix is applied to image names when using this catalog.

## See also {#section-d7c408b979844643adff8258f500eb7c}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md) 
