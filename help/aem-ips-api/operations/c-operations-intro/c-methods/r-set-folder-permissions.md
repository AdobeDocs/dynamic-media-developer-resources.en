---
description: Sets folder permissions.
seo-description: Sets folder permissions.
seo-title: setFolderPermissions
solution: Experience Manager
title: setFolderPermissions
topic: Scene7 Image Production System API
uuid: 3a33034e-df2c-48ab-8ade-b76bea444388
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
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | Company handle.  |
|  ` *`folderHandle`*`  | `xsd:string`  | Yes  | Folder handle.  |
|  ` *`setChildren`*`  | `xsd:boolean`  | Yes  | Sets permissions on children that belong to the folder.  |
|  ` *`permissionArray`*`  | `types:PermissionUpdateArray`  | Yes  | Permissions array.  |

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
