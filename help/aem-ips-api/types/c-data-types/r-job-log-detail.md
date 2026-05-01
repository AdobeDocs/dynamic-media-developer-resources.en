---
description: Job log information.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
TQID: https://experienceleague.adobe.com/HP58XyNaPK0Dpqjlyc9bS2s1NU-UFiTP32puxSMDm0s
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# [!DNL JobLogDetail]{#joblogdetail}

Job log information.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  logMessage  | `xsd:string`  | Messages in the job log.  |
|  logType  | `xsd:string`  | Job log file type.  |
|  assetName  | `xsd:string`  | Name of asset in the job log (optional).  |
|  assetType  | `xsd:string`  | Choice of asset type.  |
|  assetHandle  | `xsd:string`  | Asset handle referenced in the job log.  |
|  auxArray  | `types:JobLogDetailAuxArray`  | Provides additional detailed job log information beyond the five job log types described above.  |
