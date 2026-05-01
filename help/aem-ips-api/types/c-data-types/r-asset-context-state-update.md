---
title: AssetContextStateUpdate
description: Set a new set of publish state flags for the publish context associated with an asset.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
TQID: https://experienceleague.adobe.com/WENuvKVQR8zfR0iX-vb31wsbLgDhYJ4cfp4BCG8kInA
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

Set a new set of publish state flags for the publish context associated with an asset.

 **Parameters** 

|  Name  | Type  | Description  |
|---|---|---|
|  assetHandle  | `xsd:string`  | Handle to the asset that you want to update.  |
|  contextStateUpdateArray  | `types:ContextStateUpdateArray`  | An array of publish contact states for the asset that you want to update.  |
