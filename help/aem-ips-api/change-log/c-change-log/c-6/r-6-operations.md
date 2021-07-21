---
description: Describes new and changed operations methods for the IPS API version 6.
solution: Experience Manager
title: Operations  New and Modified
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
---
# Operations: New and Modified{#operations-new-and-modified}

Describes new and changed operations methods for the IPS API version 6.

 Syntax 

## New Operations {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts` 
* `getPublishContexts` 
* `moveFolder` 
* `setAssetsContexState` 
* `updateAssetSet` 
* `updateImageSet`

## Modified Operations {#section-f4e8755527444266ae806e3f4c851ae6}

**Added**

* Added `isHidden` and `initialTagValue` to:

  * `saveMetadataField`
  * ` `updateMetadataField``
  * `createMetadataField`

* Added `thumbAssetHandle` to:

  * `createImageSet`
  * `createAssetSet`

  Added `companyHandle` to:

  * `getViewerConfigSettings`
  * `setViewerConfigSettings`
  * `updateViewerConfigSettings`
  * `getSearchStrings`

  Added `contextHandle` to:

  * `getImageServingPublishSettings`
  * `getImageRenderingPublishSettings`
  * `setImageServingPublishSettings`
  * `setImageRenderingPublishSettings`

* Added includeInactive to:

  * `getUsers`. 
  * `getUserChars`.

* Added `permissionArray` to `createPropertySet`. 

* Added `exportJob` to `submitJob`.

**Changed**

* In `addUser` and `setUser`, changed `role` to `defaultRole`. 

* In `getCompanyMembers`, changed `userArray` to `memberArray`. 

* In `getCompanyMembership`, changed `companyArray` to `membershipArray`. 

* In `addUser`, `setCompanyMembership`, and `addCompanyMembership`, changed `membershipArray` to `companyHandleArray`. 

* In `getCompanyMembership`, changed `companyArray` to `membershipArray`. 

* In `getUserChars`, `includeInvalid` is now optional.

**Removed**

* Removed `renameFiles` from `renameAsset`. 

* Removed `getXMPPanelViewDefinition`. 
* Removed `searchAssetsByFulltext` and `searchAssetsBySimilarity`.
