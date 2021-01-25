---
description: Contains supplementary messages associated with the main job log message (JobDetail). Includes warnings and other details associated with the currently processed asset.
seo-description: Contains supplementary messages associated with the main job log message (JobDetail). Includes warnings and other details associated with the currently processed asset.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
topic: Dynamic Media Image Production System API
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
---

# JobLogDetailAux{#joblogdetailaux}

Contains supplementary messages associated with the main job log message (JobDetail). Includes warnings and other details associated with the currently processed asset.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`logMessage`*`  | `xsd:string`  | An auxiliary message.  |
|  `*`logType`*`  | `xsd:string`  |Log type: `IPSJobLog.gcUploadWarning` or `IPSJobLog.gcUploadError`.  |
|  `*`dateCreated`*`  | `xsd:dateTime`  | Auxiliary job log creation date.  |

