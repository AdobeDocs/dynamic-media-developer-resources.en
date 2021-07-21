---
description: Warning or error details for a sing update in a batchSetAssetMetadata operation.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
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
