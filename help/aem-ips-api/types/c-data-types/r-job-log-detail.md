---
description: Job log information.
seo-description: Job log information.
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
topic: Scene7 Image Production System API
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
---

# JobLogDetail{#joblogdetail}

Job log information.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  ` *`logMessage`*`  | `xsd:string`  | Messages in the job log.  |
|  ` *`logType`*`  | `xsd:string`  | Job log file type.  |
|  ` *`assetName`*`  | `xsd:string`  | Name of asset in the job log (optional).  |
|  ` *`assetType`*`  | `xsd:string`  | Choice of asset type.  |
|  ` *`assetHandle`*`  | `xsd:string`  | Asset handle referenced in the job log.  |
|  ` *`auxArray`*`  | `types:JobLogDetailAuxArray`  | Provides additional detailed job log information beyond the five job log types described above.  |

