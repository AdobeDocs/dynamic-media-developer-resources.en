---
description: Sets folder permissions.
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
TQID: 'https://experienceleague.adobe.com/r-WGRjE263vPSVKsBieklQ79SASbDQOx9hp5IzS0-O0'
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
# setFolderPermissions{#setfolderpermissions}

Sets folder permissions.

 Syntax 

## Authorized User Types {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-2a41135054954396b40f1228f2e63b42}

**Input (setFolderPermissionsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | Company handle.  |
|  folderHandle  | `xsd:string`  | Yes  | Folder handle.  |
|  setChildren  | `xsd:boolean`  | Yes  | Sets permissions on children that belong to the folder.  |
|  permissionArray  | `types:PermissionUpdateArray`  | Yes  | Permissions array.  |

**Output (setFolderPermissionsReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-01730da4be874553ab44e3241cdf6357}

This code sample specifies a company handle, a folder handle, and a permission array with detailed information about the folder. It applies the same permissions for the children of the parent folder.

**Request** 

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**Response**

None.
