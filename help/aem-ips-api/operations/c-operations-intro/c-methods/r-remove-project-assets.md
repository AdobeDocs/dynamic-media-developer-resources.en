---
description: Removes assets from a project. Does not destroy the assets.
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
TQID: 'https://experienceleague.adobe.com/GHGyYEF5H3Me5jKtkfd15Ok8KEk2hrRuVxrKCF7cZ-E'
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
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company with the assets you want to move.  |
|  projectHandle  | `xsd:string`  | Yes  | The handle to the project assets you want to move.  |
|  assetHandleArray  | `types:HandleArray`  | Yes  | Array of handles to the assets you want to move.  |

**Output (removeProjectAssetsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  successCount  | `xsd:int`  | Yes  | Successfully removed asset count.  |
|  warningCount  | `xsd:int`  | Yes  | The number of warnings generated when the operation attempted to remove assets from the project.  |
|  errorCount  | `xsd:int`  | Yes  | The number of errors generated when the operation attempted to remove assets from the project.  |
|  warningDetailArray  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated warnings when the operation attempted to remove them from the project.  |
|  errorDetailArray  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated errors when the operation attempted to remove them from the project.  |

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
