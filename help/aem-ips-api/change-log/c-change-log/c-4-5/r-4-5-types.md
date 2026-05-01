---
description: Describes new and changed data types for the IPS API version 4.5.
solution: Experience Manager
title: Data Types  New and Modified
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
TQID: https://experienceleague.adobe.com/ZTNRPCYZ9Oh9zEtcek3BOp0CX-pPC8r2ic8fcaLp11w
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
---
# Data Types: New and Modified{#data-types-new-and-modified}

Describes new and changed data types for the IPS API version 4.5.

 Syntax 

## New Types {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary` 
* `AssetSummaryArray` 
* `JobLogDetailAux` 
* `JobLogDetailAuxArray` 
* `MPEvent` 
* `MPEventArray` 
* `OperationFault` 
* `OperationFaultArray` 
* `PhotoshopOptions` 
* `TagCondition` 
* `TagConditionArray` 
* `TagFieldValues` 
* `TagFieldValuesArray` 
* `TagValueUpdate` 
* `TagValueUpdateArray` 
* `TagValueUpdateFault` 
* `TagValueUpdateFaultArray` 
* `UrlArray`

## Modified Types {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* Asset includes a new `fileName` field that returns the virtual file name. 
* `AssetSummary` returns a `type` and `name` field 

* `MetadataField` includes `isHidden`

* `MetadataUpdate` 
* `UploadUrlsJob` requires a `urlArray` and adds an optional `numUrls` count
