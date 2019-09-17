---
description: Describes new and changed operations methods for the IPS API version 3.7.
seo-description: Describes new and changed operations methods for the IPS API version 3.7.
seo-title: Operations  New and Modified
solution: Experience Manager
title: Operations  New and Modified
topic: Scene7 Image Production System API
uuid: 3c163157-cd0d-4887-a1f0-7941d96c36f9
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

