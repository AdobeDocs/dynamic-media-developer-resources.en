---
description: Layer view properties.
seo-description: Layer view properties.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# LayerViewInfo{#layerviewinfo}

Layer view properties.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`url`*`  | `xsd:string`  |Image server URL that represents the template. Combines `urlModifier` and `urlPostAp- plyModifier` fields.  |
|  `*`urlModifier`*`  | `xsd:string`  |Image serving protocol commands to apply prior to request or `urlPostApplyModifier` commands.  |
|  `*`urlPostApplyModifier`*`  | `xsd:string`  |Image serving protocol commands to apply after `urlModifier` and request commands.  |

