---
description: Prefix request modifier string. None or more Image Serving commands separated by '&' characters.
seo-description: Prefix request modifier string. None or more Image Serving commands separated by '&' characters.
seo-title: Modifier
solution: Experience Manager
title: Modifier
topic: Scene7 Image Serving - Image Rendering API
uuid: eb17d115-22ec-4b1b-9039-9bd2bc256f48
index: y
internal: n
snippet: y
---

# Modifier{#modifier}

Prefix request modifier string. None or more Image Serving commands separated by '&' characters.

 Used to persistently modify images and store the body of templates.

Commands in this field are overridden by the same commands in the request or template from which this record is referenced, and by commands in `catalog::PostModifier`

Macros are permitted in `catalog::Modifier`, as long as they are defined in the same catalog or in the default catalog. Custom variables may be used as well.

## Properties {#section-6674388f77d644469371a17e8809c45f}

Text string. Optional.

## Default {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

None.

## See also {#section-7a67803d141b442180c418c1f3cff029}

[catalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b) 
