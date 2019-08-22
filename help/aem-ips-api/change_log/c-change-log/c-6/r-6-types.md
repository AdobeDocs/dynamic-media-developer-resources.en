---
description: Describes new and changed types for the IPS API version 6.
seo-description: Describes new and changed types for the IPS API version 6.
seo-title: Data Types  New and Modified
solution: Experience Manager
title: Data Types  New and Modified
topic: Scene7 Image Production System API
uuid: 6cc7fc9d-e259-49db-91ed-cf67d811e627
index: y
internal: n
snippet: y
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

