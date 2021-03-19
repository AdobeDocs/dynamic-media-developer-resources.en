---
description: Watermark selector. Specifies the catalog Id of the catalog record to be used as a watermark image or template.
seo-description: Watermark selector. Specifies the catalog Id of the catalog record to be used as a watermark image or template.
seo-title: Watermark
solution: Experience Manager
title: Watermark
uuid: 18add7ab-0797-4ab3-a7e8-05c745abe605
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Watermark{#watermark}

Watermark selector. Specifies the catalog::Id of the catalog record to be used as a watermark image or template.

 If specified, the server applies the watermark to the requested image data for all image requests ( `req=img`).

## Properties {#section-fad6ffff4c5f4b5c8010281bc1377055}

Text string. If specified, must be a valid `Catalog::Id` value in this image catalog (or in the default catalog, if specified in [!DNL default.ini]).

## Default {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Inherited from `default::Watermark` if not defined. If defined but empty, no watermarking is applied for this image catalog, even if `default::Watermark` is defined.

## See also {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md) 
