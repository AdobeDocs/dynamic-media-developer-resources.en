---
description: Hierarchical file or asset storage object. Folders can contain one (or more) subfolders.
solution: Experience Manager
title: Folder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
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
