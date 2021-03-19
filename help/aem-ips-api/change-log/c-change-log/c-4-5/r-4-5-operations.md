---
description: Describes new and changed operations methods for the IPS API version 4.5.
solution: Experience Manager
title: Operations  New and Modified
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# Operations: New and Modified{#operations-new-and-modified}

Describes new and changed operations methods for the IPS API version 4.5.

 Syntax 

## New Operations {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent` 
* `addTagFieldValues` 
* `cdnCacheInvalidation` 
* `deleteTagFieldValues` 
* `deleteTagFieldValues` 
* `getDistinctMetadataValues` 
* `getMediaPortalEvent` 
* `getTagFieldValues` 
* `getXMPPacket` 
* `searchAssetsByFullText` 
* `searchAssetsByMetadata` 
* `setTagFieldValues` 
* `updateTagFieldValues` 
* `updateXMPPacket`

## Modified Operations {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` includes `animatedGifInfo`, `swcInfo`, `cssInfo`, and `javascriptInfo` parameters. 

* `createMetadataField` includes an optional `isHidden` parameter. 

* `saveMetadataField` includes an optional `isHidden` parameter. 

* `searchAssets` 
* 
* The `renameFiles` parameter has been deprecated for prior releases and removed from the `renameAsset` operation. The virtual file path is changed to match the new asset name (preserving the file extension), while physical file paths are not affected. API clients need to remove references to this parameter when updating to the new API version.

