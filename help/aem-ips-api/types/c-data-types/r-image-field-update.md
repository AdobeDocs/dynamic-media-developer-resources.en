---
description: Updates the image field associated with an image asset.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
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
