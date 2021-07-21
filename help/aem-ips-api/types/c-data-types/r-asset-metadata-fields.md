---
description: Returns metadata field definitions for specified asset types.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
---
# AssetMetadataFields{#assetmetadatafields}

Returns metadata field definitions for specified asset types.

 Syntax 

## Parameters {#section-5ad771540c5f40c187b35e34aac19305}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`assetType`*`  | `xsd:string`  | Asset type associated with field definitions (see "Asset Types" for values).  |
|  `*`fieldArray`*`  | `types:MetadataFieldArray`  |Array of metadata field definitions associated with the asset type specified in `assetType`.  |
