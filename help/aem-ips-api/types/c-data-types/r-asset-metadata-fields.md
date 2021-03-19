---
description: Returns metadata field definitions for specified asset types.
seo-description: Returns metadata field definitions for specified asset types.
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
feature: "Dynamic Media Classic,SDK/API,Metadata,Asset Management"
role: "Developer,Administrator"
---

# AssetMetadataFields{#assetmetadatafields}

Returns metadata field definitions for specified asset types.

 Syntax 

## Parameters {#section-5ad771540c5f40c187b35e34aac19305}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`assetType`*`  | `xsd:string`  | Asset type associated with field definitions (see "Asset Types" for values).  |
|  `*`fieldArray`*`  | `types:MetadataFieldArray`  |Array of metadata field definitions associated with the asset type specified in `assetType`.  |

