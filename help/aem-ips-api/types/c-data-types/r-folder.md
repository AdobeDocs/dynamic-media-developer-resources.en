---
description: Hierarchical file or asset storage object. Folders can contain one (or more) subfolders.
seo-description: Hierarchical file or asset storage object. Folders can contain one (or more) subfolders.
seo-title: Folder
solution: Experience Manager
title: Folder
topic: Scene7 Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
index: y
internal: n
snippet: y
---

# Folder{#folder}

Hierarchical file or asset storage object. Folders can contain one (or more) subfolders.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  ` *`folderHandle`*`  | `xsd:string`  | Folder handle.  |
|  ` *`path`*`  | `xsd:string`  | Folder path.  |
|  ` *`lastModified`*`  | `xsd:dateTime`  | Last modification date.  |
|  ` *`childLastModified`*`  | `xsd:dateTime`  | Last modification date for subfolders and folder child assets.  |
|  ` *`permissionsSetHandle`*`  | `xsd:string`  | Folder permissions handle.  |
|  ` *`hasSubfolder`*`  | `types:Boolean`  | Determines if a folder has subfolders.  |
|  ` *`subfolderArray`*`  | `types:FolderArray`  | An array of subfolders in a folder.  |

