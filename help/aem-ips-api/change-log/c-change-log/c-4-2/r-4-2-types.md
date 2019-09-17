---
description: Describes new and changed data types for the IPS API version 4.2.
seo-description: Describes new and changed data types for the IPS API version 4.2.
seo-title: Data Types  New and Modified
solution: Experience Manager
title: Data Types  New and Modified
topic: Scene7 Image Production System API
uuid: 274e49da-9eb8-4082-971c-056acb47a53e
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

