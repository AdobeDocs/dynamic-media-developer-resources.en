---
description: Layer view properties.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
---
# [!DNL LayerViewInfo]{#layerviewinfo}

Layer view properties.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  url  | `xsd:string`  |Image server URL that represents the template. Combines `urlModifier` and `urlPostAp- plyModifier` fields.  |
|  urlModifier  | `xsd:string`  |Image serving protocol commands to apply prior to request or `urlPostApplyModifier` commands.  |
|  urlPostApplyModifier  | `xsd:string`  |Image serving protocol commands to apply after `urlModifier` and request commands.  |
