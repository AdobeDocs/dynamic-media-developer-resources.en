---
description: Describes new and changed data types for the IPS API version 4.2.
solution: Experience Manager
title: Data Types  New and Modified
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
TQID: 'https://experienceleague.adobe.com/2YCgrii3dF6Zq7NlXRI0vD3DtO-jWpSo4YKcpZsdFHU'
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
---
# Data Types: New and Modified{#data-types-new-and-modified}

Describes new and changed data types for the IPS API version 4.2.

 Syntax 

## New Types {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo` 
* `CuePointInfo` 
* `PdfSettings` 
* `PremeierExpressRemixInfo`

## Modified Types {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**Asset**

Parameters added:

* `readyForPublish` 
* `trashState` 
* `MaskInfo` 
* `RTFInfo`

Parameters removed:

* `ImageSetInfo` 
* `RenderSetInfo`

**ReprocessAssetsJob**

Parameters added:

* `preservePublishState` 
* `preserveCrop` 
* `readyForPublish`

**UploadDirectoryJob**

Parameters added:

* `preservePublishState` 
* `preserveCrop` 
* `videoEncodingPreset`

**UploadUrlsJob**

Parameters added:

* `preservePublishState` 
* `preserveCrop`

