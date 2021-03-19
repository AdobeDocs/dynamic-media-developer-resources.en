---
description: Updates asset permissions.
seo-description: Updates asset permissions.
seo-title: updateAssetPermissons
solution: Experience Manager
title: updateAssetPermissons
uuid: feb2faf3-81de-436e-82de-1e41df03508f
feature: "Dynamic Media Classic,SDK/API,Asset Management"
role: "Developer,Administrator"
---

# updateAssetPermissons{#updateassetpermissons}

Updates asset permissions.

 Syntax 

## Authorized User Types {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-392cb3076cf84790a32fd913f2b111a3}

**Input (updateAssetPermissionsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | Company handle.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | Asset handle.  |
|  `*`updateArray`*`  | `types:PermissionUpdateArray`  | Yes  | Permissions you want to apply to the asset.  |

**Output (updateAssetPermissionsReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**Request** 

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**Response**

None. 
