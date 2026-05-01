---
description: Describes new and changed types for the IPS API version 6.
solution: Experience Manager
title: Data Types  New and Modified
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
TQID: https://experienceleague.adobe.com/AgiiuIF59Pj7z8kNJO6Ixf5Ou8zbuPSH9Qeh2w-pWL8
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

Describes new and changed types for the IPS API version 6.

 Syntax 

## New Types {#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate` 
* `AssetContextStateUpdateArray` 
* `AssetPublishContexts` 
* `AssetPublishContextsArray` 
* `CompanyMember` 
* `CompanyMemberArray` 
* `CompanyMembershipUpdate` 
* `CompanyMembershipUpdateArray` 
* `ContextStateUpdate` 
* `ContextStateUpdateArray` 
* `Export Job` 
* `PermissionsSet` 
* `PermissionsSetArray` 
* `PublishContext` 
* `PublishContextArray`

## Modified Types {#section-56b834b1a3b843279d8715b4a4f3890b}

**Added**

* Added `numUrls` to `UploadUrlsJob`. 

* Added `fileName` to `Asset.`

* Added `isHidden` to `MetadataField`. 

* Added `taskState` to `TaskProgress`. 

* Added `exportJob` to `ActiveJob` and `ScheduledJob`. 

* Added `optmizedPath` and `optimizedFile` to `PsdInfo`. 

* Added `contextHandle` to:

  * `ImageRenderingPublishJob`
  * `VideoPublishJob`

* Added the following parameters to `Asset`:

  * `animatedGifInfo`
  * `swcInfo`
  * `cssInfo`
  * `javascriptInfo`

**Changed**

* In `User`, changed `role` to `defaultRole`. 

* In `Folder`, changed `permissions` to `permissionsSetHandle`. 

* In `AssetSummary`, `type` and `name` are now optional.
