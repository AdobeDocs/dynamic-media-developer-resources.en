---
description: Thumbnail resolution. Specifies the object resolution for the thumbnail image.
seo-description: Thumbnail resolution. Specifies the object resolution for the thumbnail image.
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
topic: Scene7 Image Serving - Image Rendering API
uuid: 10bbad31-a0fd-4ed3-b708-87822777acdd
---

# ThumbRes{#thumbres}

Thumbnail resolution. Specifies the object resolution for the thumbnail image.

 Only used if `catalog::ThumbType=3`.

## Properties {#section-ee5cae086a3d4875805fa8a08756a586}

Real number value greater than 0. Must have the same units as `catalog::Resolution`.

## Default {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` is used if the field is not present, if the value is 0 or if the field is empty.

## See also {#section-eb716bf647614db083020fe8ce453751}

[catalog:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) , [catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [attribute::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f) 
