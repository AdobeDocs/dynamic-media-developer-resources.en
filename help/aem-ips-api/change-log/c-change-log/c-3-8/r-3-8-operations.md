---
description: Describes new and changed operations methods for the IPS API version 3.8.
solution: Experience Manager
title: Operations  New and Modified
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
TQID: https://experienceleague.adobe.com/3wKOXTaVJQS2w-c4pqrH2r-7fEPqKyuTlaEwQYTQe-s
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Operations: New and Modified{#operations-new-and-modified}

Describes new and changed operations methods for the IPS API version 3.8.

 Syntax 

## New Operations {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState` 
* `saveZoomTarget` 
* `deleteZoomTarget` 
* `saveImageMap` 
* `deleteImageMap` 
* `createImageSet` 
* `getImageSetMembers`

## Modified Operations {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* The optional `publishState` parameter lets you search on the `MarkedForPublish/NotMarkedForPublish` asset state.

**getJobLogs**

* The optional `userHandle` parameter lets you retrieve job logs submitted by a specific user.
