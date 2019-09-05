---
description: Watermark selector. Specifies the catalog Id of the catalog record to be used as a watermark image or template.
seo-description: Watermark selector. Specifies the catalog Id of the catalog record to be used as a watermark image or template.
seo-title: Watermark
solution: Experience Manager
title: Watermark
topic: Scene7 Image Serving - Image Rendering API
uuid: ed0faa2f-ae6b-4ffb-9043-5856cf3fdd4e
index: y
internal: n
snippet: y
---

# Watermark{#watermark}

Watermark selector. Specifies the catalog::Id of the catalog record to be used as a watermark image or template.

 If specified, the server applies the watermark to the requested image data for all image requests ( `req=img`).

## Properties {#section-fad6ffff4c5f4b5c8010281bc1377055}

Text string. If specified, must be a valid `Catalog::Id` value in this image catalog (or in the default catalog, if specified in [!DNL default.ini]).

## Default {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Inherited from `default::Watermark` if not defined. If defined but empty, no watermarking is applied for this image catalog, even if `default::Watermark` is defined.

## See also {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](r_id_cat.md#reference_C3F3CE9AAAC4451796A846D6722383E5) 
