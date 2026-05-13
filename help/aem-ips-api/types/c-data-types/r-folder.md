---
description: Hierarchical file or asset storage object. Folders can contain one (or more) subfolders.
solution: Experience Manager
title: Folder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
TQID: 'https://experienceleague.adobe.com/nh6zqOnt-bxAFmsHSHPRCMThKlOwi-9b9fep6ujKZyE'
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
# [!DNL Folder]{#folder}

Hierarchical file or asset storage object. Folders can contain one (or more) subfolders.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  folderHandle  | `xsd:string`  | Folder handle.  |
|  [!DNL path]  | `xsd:string`  | Folder path.  |
|  lastModified  | `xsd:dateTime`  | Last modification date.  |
|  childLastModified  | `xsd:dateTime`  | Last modification date for subfolders and folder child assets.  |
|  permissionsSetHandle  | `xsd:string`  | Folder permissions handle.  |
|  hasSubfolder  | `types:Boolean`  | Determines if a folder has subfolders.  |
|  subfolderArray  | `types:FolderArray`  | An array of subfolders in a folder.  |
