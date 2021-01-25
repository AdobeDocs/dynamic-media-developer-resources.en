---
description: Removes assets from a project. Does not destroy the assets.
seo-description: Removes assets from a project. Does not destroy the assets.
seo-title: removeProjectAssets
solution: Experience Manager
title: removeProjectAssets
topic: Dynamic Media Image Production System API
uuid: bae09dc3-4328-4264-8fb2-e4f0c53546eb
---

# removeProjectAssets{#removeprojectassets}

Removes assets from a project. Does not destroy the assets.

 Syntax 

## Authorized User Types {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-169d8e317417415b87df86242f65710e}

**Input (removeProjectAssetsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company with the assets you want to move.  |
|  `*`projectHandle`*`  | `xsd:string`  | Yes  | The handle to the project assets you want to move.  |
|  `*`assetHandleArray`*`  | `types:HandleArray`  | Yes  | Array of handles to the assets you want to move.  |

**Output (removeProjectAssetsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`successCount`*`  | `xsd:int`  | Yes  | Successfully removed asset count.  |
|  `*`warningCount`*`  | `xsd:int`  | Yes  | The number of warnings generated when the operation attempted to remove assets from the project.  |
|  `*`errorCount`*`  | `xsd:int`  | Yes  | The number of errors generated when the operation attempted to remove assets from the project.  |
|  `*`warningDetailArray`*`  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated warnings when the operation attempted to remove them from the project.  |
|  `*`errorDetailArray`*`  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated errors when the operation attempted to remove them from the project.  |

## Examples {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

This code sample removes 2 assets from a project (specified by the project handle).

**Request** 

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```

