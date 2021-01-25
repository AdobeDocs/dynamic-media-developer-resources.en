---
description: Renames a folder.
seo-description: Renames a folder.
seo-title: renameFolder
solution: Experience Manager
title: renameFolder
topic: Dynamic Media Image Production System API
uuid: 7d190a57-1d81-4f41-9205-b8ffdf7330ec
---

# renameFolder{#renamefolder}

Renames a folder.

 Syntax 

## Authorized User Types {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read and write access to the asset.

## Parameters {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**Input (renameFolderParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | Handle to the company with folders you want to rename.  |
|  `*`folderHandle`*`  | `xsd:string`  | Yes  | Handle to the folder.  |
|  `*`folderName`*`  | `xsd:string`  | Yes  | New folder name.  |

**Output (renameFolderReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`folderHandle`*`  | `xsd:string`  | Yes  | Handle to the renamed folder.  |

## Examples {#section-98bdd2f88d164f488676e90aba1dc864}

This code sample renames a folder.

**Request** 

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**Response** 

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```

