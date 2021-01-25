---
description: Mask file path. Relative or absolute path and name for a mask image file associated with this catalog record.
seo-description: Mask file path. Relative or absolute path and name for a mask image file associated with this catalog record.
seo-title: MaskPath
solution: Experience Manager
title: MaskPath
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a2d1f08a-0a26-41a6-9be2-f5cc2afb15c4
---

# MaskPath{#maskpath}

Mask file path. Relative or absolute path and name for a mask image file associated with this catalog record.

Allows attaching separate masks to images.

The server uses the path resolution rules described in [Managing Source Data](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) to find the data file.

## Properties {#section-cdc3b7e2811e41008479cd97887c01b7}

Text string value. Optional. If specified, it must be a valid relative or absolute Image Server file path. `attribute::DefaultExt` is appended if no file suffix is present.

If both a main image ( `catalog::Path`) and a mask image ( `catalog::MaskPath`) are defined in a catalog record, both must have exactly the same pixel size. Mask images must be 8-bit grayscale.

`mask=` in the request overrides `catalog::MaskPath`.

`catalog::MaskPath` overrides the alpha channel in the main image ( `catalog::Path`), if present, and if the alpha channel is unassociated (i.e. not pre-multiplied). If the image alpha is pre-multiplied, `catalog::MaskPath` is ignored and the alpha channel is always used.

## Default {#section-78533e35bfec469ba087cb68a35bb81b}

None.

## See also {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) 
