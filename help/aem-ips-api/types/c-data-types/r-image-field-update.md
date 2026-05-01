---
description: Updates the image field associated with an image asset.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
TQID: https://experienceleague.adobe.com/nkT5je1o5RQU6GdVwmgc7lgY89w4yXx6c-n4ow1TAcQ
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
# [!DNL ImageFieldUpdate]{#imagefieldupdate}

Updates the image field associated with an image asset.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  assetHandle  | `xsd:string`  | Asset handle.  |
|  [!DNL resolution]  | `xsd:double`  | Image resolution in pixels per inch.  |
|  [!DNL anchorX]  | `xsd:int`  | X axis image anchor.  |
|  [!DNL anchorY]  | `xsd:int`  | Y axis image anchor.  |
|  [!DNL userData]  | `xsd:string`  |Value of `userData` metadata field, which is published to the image serving user data catalog field.  |
