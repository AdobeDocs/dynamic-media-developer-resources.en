---
title: AssetContextStateUpdate
description: Set a new set of publish state flags for the publish context associated with an asset.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
---
# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

Set a new set of publish state flags for the publish context associated with an asset.

 **Parameters** 

|  Name  | Type  | Description  |
|---|---|---|
|  assetHandle  | `xsd:string`  | Handle to the asset that you want to update.  |
|  contextStateUpdateArray  | `types:ContextStateUpdateArray`  | An array of publish contact states for the asset that you want to update.  |
