---
description: Describes new and changed operations methods for the IPS API version 3.7.
solution: Experience Manager
title: Operations  New and Modified
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
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
