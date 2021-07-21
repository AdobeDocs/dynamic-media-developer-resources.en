---
description: Describes new and changed data types for the IPS API version 4.5.
solution: Experience Manager
title: Data Types  New and Modified
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
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
