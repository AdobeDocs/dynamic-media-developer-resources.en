---
description: Sets the permissions of a single asset by using a permission asset.
seo-description: Sets the permissions of a single asset by using a permission asset.
seo-title: setAssetPermissions
solution: Experience Manager
title: setAssetPermissions
uuid: 38f26482-bce9-4d2c-9714-e8c3ae40c2d1
feature: "Dynamic Media Classic,SDK/API,Asset Management"
role: "Developer,Administrator"
---

# setAssetPermissions{#setassetpermissions}

Sets the permissions of a single asset by using a permission asset.

 Assets inherit the permissions of their parent folder by default. Once you set permissions on an asset, it no longer inherits the permissions of its parent unless you call `removeAssetPermissions`. 

## Authorized User Types {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-e05abbce6453450fb38747101cb5e228}

**Input (setAssetPermissonsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company that contains the folder you want to work with.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | Folder handle.  |
|  `*`permissionArray`*`  | `types:PermissionsUpdateArray`  | Yes  | Permissions array.  |

**Output (setAssetPermissonsReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-38955bc330bb4909b6b06027ef2b143e}

This code sample sets permissions on an asset. It contains the company and asset handle, and a permissions array.

**Request** 

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**Response**

None. 
