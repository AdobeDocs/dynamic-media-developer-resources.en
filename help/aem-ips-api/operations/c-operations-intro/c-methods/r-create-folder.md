---
title: createFolder
description: Creates a folder.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
TQID: 'https://experienceleague.adobe.com/iQNFDdsbxhklGSfUb1pmcNhzIT8kJYc19xFglU7Blc8'
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
# [!DNL createFolder]{#createfolder}

Creates a folder.

>[!NOTE]
>
>The new folder is subordinate to the Images folder, even if you specify a `/` to indicate the root of the company.

Syntax 

## Authorized User Types {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read/write access to the parent folder.

## Parameters {#section-c00d8d89cf114886a535056f2a1bf892}

**Input (createFolder)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The Handle to the company  |
|  folderPath  | `xsd:string`  | Yes  | The root folder used to retrieve folders and all subfolders to the leaf level. If excluded, the company root is used.  |

**Output (createFolderParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  folderHandle  | `xsd:string`  | Yes  | Handle of the new folder.  |

## Examples {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

This sample code creates a folder at the root of a company. The response returns the handle of the newly created folder.

**Request** 

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**Response** 

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```
