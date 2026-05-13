---
description: Describes new and changed operations methods for the IPS API version 3.7.
solution: Experience Manager
title: Operations  New and Modified
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
TQID: 'https://experienceleague.adobe.com/nt-KwoxJw8bSbt076MIIZlXW2YbMzwVURLwE-94hlDU'
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
# Operations: New and Modified{#operations-new-and-modified}

Describes new and changed operations methods for the IPS API version 3.7.

 Syntax 

## New Operations {#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset` 
* `renameAsset` 
* `deleteAsset` 
* `createFolder` 
* `deleteFolder` 
* `getActiveJobs` 
* `getScheduledJobs` 
* `getJobLogs` 
* `getJbLogDetails` 
* `submitJob` 
* `stopJob` 
* `pauseJob` 
* `resumeJob` 
* `executeJob` 
* `deleteJob`

## Modified Operations {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* Removed `name` parameter. 
* Added `excludeFieldArray`.

**getFolders**

* Added `excludeFieldArray`.

**getFolderTree**

* Added `excludeFieldArray` and `getUniqueMetadataValues`. 
* Made `fieldHandle` a required parameter.
