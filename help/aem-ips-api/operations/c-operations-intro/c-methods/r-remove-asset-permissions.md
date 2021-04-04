---
description: Removes permissions from selected assets.
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
exl-id: c47d9853-91b1-45fe-b8ff-aaa1239ca0d1
---
# removeAssetPermissions{#removeassetpermissions}

Removes permissions from selected assets.

 Syntax 

## Authorized User Types {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**Input (removeAssetPermissionsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | The handle to the asset with permissions you want to remove.  |

**Output (removeAssetPermissionsReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-238fa7bb091548f5ba72ced11fc92d4f}

This code sample removes permissions from an asset.

**Request** 

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Response**

None.
