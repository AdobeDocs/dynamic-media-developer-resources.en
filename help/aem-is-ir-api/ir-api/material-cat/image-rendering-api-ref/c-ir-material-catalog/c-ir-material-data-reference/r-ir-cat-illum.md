---
description: Illumination map selector. Allows explicit selection of the illumination map to be used when rendering this material.
seo-description: Illumination map selector. Allows explicit selection of the illumination map to be used when rendering this material.
seo-title: Illum
solution: Experience Manager
title: Illum
topic: Scene7 Image Serving - Image Rendering API
uuid: 2df0abbb-0d54-41b7-80c4-b914c18cd1b1
index: y
internal: n
snippet: y
---

# Illum{#illum}

Illumination map selector. Allows explicit selection of the illumination map to be used when rendering this material.

## Properties {#section-162bcf562ca844ccba9e81e267508cca}

Enum. Set to -1 for automatic selection of the illumination map based on the value of catalog::Gloss.

Set to 0, 1, or 2 to select illumination map A, B, or C. The renderer will choose the closest illumination map available in the vignette.

## Default {#section-ac386d31ef90423b8a367010a60bddc7}

-1 (automatic selection)

## See also {#section-d9db8507a5e54692b84f54b3f84b782a}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb) 
