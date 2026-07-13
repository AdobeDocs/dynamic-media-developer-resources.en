---
description: Sets the permissions of a single asset by using a permission asset.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
TQID: 'https://experienceleague.adobe.com/dd96ai2DgoCqZ1NR-2rixSHDEaBSgk6ioQIqmG-1RoE'
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
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company that contains the folder you want to work with.  |
|  assetHandle  | `xsd:string`  | Yes  | Folder handle.  |
|  permissionArray  | `types:PermissionsUpdateArray`  | Yes  | Permissions array.  |

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

