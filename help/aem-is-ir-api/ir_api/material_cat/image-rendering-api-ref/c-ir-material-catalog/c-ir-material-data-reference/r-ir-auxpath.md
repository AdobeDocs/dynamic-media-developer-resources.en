---
description: Data file path. Relative path and name for non-image data files associated with this image.
seo-description: Data file path. Relative path and name for non-image data files associated with this image.
seo-title: AuxPath
solution: Experience Manager
title: AuxPath
topic: Scene7 Image Serving - Image Rendering API
uuid: c80720ed-48f8-4d1a-97f2-5b474f926e38
index: y
internal: n
snippet: y
---

# AuxPath{#auxpath}

Data file path. Relative path and name for non-image data files associated with this image.

The server combines this value with attribute::RootPath to build the actual file path. May also be an absolute file path.

Used to specify a cabinet style file for a cabinet material or a window covering style file for a window covering material. Leave empty for all other materials.

## Properties {#section-4268350054b7421da0ce0327f0731a52}

Text string value. If specified, it must be a valid relative or absolute file path. Required for cabinet materials and window covering materials. Must be empty for all other materials.

## Default {#section-287005c2d8e948fa958f69ba7b90b437}

None.

## See also {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute::RootPath](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [catalog::Path](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590), [src=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) 
