---
description: PostScript file properties.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# GenerationInfo{#generationinfo}

PostScript file properties.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`engine`*`  | `xsd:string`  | Generation engine used (see "Generation Info" for values).  |
|  `*`originator`*`  | `types:Asset`  | Asset record of the primary asset used in the generation.  |
|  `*`generated`*`  | `types:Asset`  | Asset record of the generated asset.  |
|  `*`attributeArray`*`  | `types:GenerationAttributeArray`  | Array of attributes associated with the generation process.  |

