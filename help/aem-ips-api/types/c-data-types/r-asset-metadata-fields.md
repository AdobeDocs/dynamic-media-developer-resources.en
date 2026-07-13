---
title: AssetMetadataFields
description: Returns metadata field definitions for specified asset types.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
TQID: 'https://experienceleague.adobe.com/U9JVe27HBTMtlBXmwDnkVAOaVfsBspa5r5fvnQl-h58'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
---
# [!DNL AssetMetadataFields]{#assetmetadatafields}

Returns metadata field definitions for specified asset types.

 Syntax 

## Parameters {#section-5ad771540c5f40c187b35e34aac19305}

|  Name  | Type  | Description  |
|---|---|---|
|  assetType  | `xsd:string`  | Asset type associated with field definitions (see "Asset Types" for values).  |
|  fieldArray  | `types:MetadataFieldArray`  | Array of metadata field definitions associated with the asset type specified in `assetType`.  |

