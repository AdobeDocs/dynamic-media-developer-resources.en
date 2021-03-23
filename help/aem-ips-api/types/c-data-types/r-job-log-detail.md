---
description: Job log information.


solution: Experience Manager
title: JobLogDetail

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# JobLogDetail{#joblogdetail}

Job log information.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`logMessage`*`  | `xsd:string`  | Messages in the job log.  |
|  `*`logType`*`  | `xsd:string`  | Job log file type.  |
|  `*`assetName`*`  | `xsd:string`  | Name of asset in the job log (optional).  |
|  `*`assetType`*`  | `xsd:string`  | Choice of asset type.  |
|  `*`assetHandle`*`  | `xsd:string`  | Asset handle referenced in the job log.  |
|  `*`auxArray`*`  | `types:JobLogDetailAuxArray`  | Provides additional detailed job log information beyond the five job log types described above.  |

