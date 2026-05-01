---
description: Move a folder to a new location.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
TQID: https://experienceleague.adobe.com/JZndHp9WkIab4mEUtsHHFnqfFBqth7Qlne9kHIW9abk
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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
|  companyHandle  | `xsd:string`  | Yes  | Handle to the company.  |
|  folderHandle  | `xsd:string`  | Yes  | Folder handle.  |
|  destFolderHandle  | `xsd:string`  | Yes  | Handle to the destination folder.  |

**Output (moveFolderReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  folderHandle  | `xsd:string`  | Yes  | Handle to the moved folder.  |

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
