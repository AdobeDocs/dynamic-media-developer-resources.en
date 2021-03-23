---
description: Catalog identifier. The HTTP path element to be used to identifies this catalog in the vignette, material, or ICC profile object specifier in HTTP requests.


solution: Experience Manager
title: RootId

feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# RootId{#rootid}

Catalog identifier. The HTTP path element to be used to identifies this catalog in the vignette, material, or ICC profile object specifier in HTTP requests.

## Properties {#section-c33266223d5b47029df756caa4e0df0c}

Text string value. May include any characters which are valid in http paths.

## Default {#section-e0ed902557684345850b86672b5dbe5b}

None. Each catalog must have a unique `catalog::RootId` value. default.ini typically has an empty `catalog::RootId`.

## See also {#section-4670832574f54f9080bb485b047efd5b}

[catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85) , [vignette::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-id-vignette.md#reference-2a7ba758924b4757b3234942304db7fd), [profile::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-macro-definition-reference/r-ir-name.md#reference-63b663d2052545ffab030a23e7060b1e), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) 
