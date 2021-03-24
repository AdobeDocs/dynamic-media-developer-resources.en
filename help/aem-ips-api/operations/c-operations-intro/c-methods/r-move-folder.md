---
description: Move a folder to a new location.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# moveFolder{#movefolder}

Move a folder to a new location.

 Syntax 

## Authorized User Types {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-473c2e68bcc14a9ea2593bee26e679dd}

**Input (moveFolderParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | Handle to the company.  |
|  `*`folderHandle`*`  | `xsd:string`  | Yes  | Folder handle.  |
|  `*`destFolderHandle`*`  | `xsd:string`  | Yes  | Handle to the destination folder.  |

**Output (moveFolderReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`folderHandle`*`  | `xsd:string`  | Yes  | Handle to the moved folder.  |

## Examples {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Request** 

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**Response** 

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```

