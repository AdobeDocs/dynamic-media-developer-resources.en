---
description: Postfix request modifier string. None or more Image Serving commands separated by '&' characters.
seo-description: Postfix request modifier string. None or more Image Serving commands separated by '&' characters.
seo-title: PostModifier
solution: Experience Manager
title: PostModifier
topic: Scene7 Image Serving - Image Rendering API
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
---

# PostModifier{#postmodifier}

Postfix request modifier string. None or more Image Serving commands separated by '&' characters.

Commands in this field always override commands in the HTTP request and in `catalog::Modifier`.

`catalog::PostModifier` is useful if certain images require special settings which are normally controlled from the URL, such as `qlt=` or `resmode=`. `catalog::Modifier` should be used for setting most IS commands in the image catalog.

Macros are permitted in `catalog::PostModifier`, as long as they are defined in the same catalog or in the default catalog. Custom variables may be used as well.

>[!NOTE]
>
>If a request involves multiple layers, only the contents of `catalog::PostModifier` of layer 0 is applied. `catalog::PostModifier` of all other layers is ignored.

## Properties {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Text string. Optional.

## Default {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

None.

## See also {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834) 
