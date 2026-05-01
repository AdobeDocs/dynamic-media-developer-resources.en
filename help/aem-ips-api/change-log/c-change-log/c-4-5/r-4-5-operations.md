---
description: Describes new and changed operations methods for the IPS API version 4.5.
solution: Experience Manager
title: Operations -  New and Modified
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
TQID: https://experienceleague.adobe.com/Af23l1YhdgJkDQeSt0sShZBdPHiQpOQvODtL-3oA-as
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
* The `renameFiles` parameter has been deprecated for prior releases and removed from the `renameAsset` operation. The virtual file path is changed to match the new asset name (preserving the file extension), while physical file paths are not affected. API clients need to remove references to this parameter when updating to the new API version.
