---
description: Warning or error details for a sing update in a batchSetAssetMetadata operation.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
TQID: 'https://experienceleague.adobe.com/kqC7eTmOZHNIYAn8yTKr-q-rJMQMzqBC9moArFK9no4'
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
# [!DNL SetMetadataFault]{#setmetadatafault}

Warning or error details for a sing update in a batchSetAssetMetadata operation.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  assetHandle  | `xsd:string`  | The asset whose metadata was unsuccessfully set.  |
|  fieldHandle  | `xsd:string`  | The handle to the metadata field whose value was unsuccessfully set.  |
|  code  | `xsd:int`  | Fault code.  |
|  reason  | `xsd:string`  | Fault description (plain-text).  |

