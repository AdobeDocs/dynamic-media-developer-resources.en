---
description: Warning or error details for a sing update in a batchSetAssetMetadata operation.
seo-description: Warning or error details for a sing update in a batchSetAssetMetadata operation.
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Dynamic Media Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
---

# SetMetadataFault{#setmetadatafault}

Warning or error details for a sing update in a batchSetAssetMetadata operation.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`assetHandle`*`  | `xsd:string`  | The asset whose metadata was unsuccessfully set.  |
|  `*`fieldHandle`*`  | `xsd:string`  | The handle to the metadata field whose value was unsuccessfully set.  |
|  `*`code`*`  | `xsd:int`  | Fault code.  |
|  `*`reason`*`  | `xsd:string`  | Fault description (plain-text).  |

