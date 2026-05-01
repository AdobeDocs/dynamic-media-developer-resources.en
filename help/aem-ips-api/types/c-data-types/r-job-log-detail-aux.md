---
description: Contains supplementary messages associated with the main job log message (JobDetail). Includes warnings and other details associated with the currently processed asset.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
TQID: https://experienceleague.adobe.com/8e2-gKGAOWq1ox1rNolyzQK0EKbfbl3BbA8DbfFMtl0
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# [!DNL JobLogDetailAux]{#joblogdetailaux}

Contains supplementary messages associated with the main job log message (JobDetail). Includes warnings and other details associated with the currently processed asset.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  logMessage  | `xsd:string`  | An auxiliary message.  |
|  logType  | `xsd:string`  |Log type: `IPSJobLog.gcUploadWarning` or `IPSJobLog.gcUploadError`.  |
|  dateCreated  | `xsd:dateTime`  | Auxiliary job log creation date.  |
