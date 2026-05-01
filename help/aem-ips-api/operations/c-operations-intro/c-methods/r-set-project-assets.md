---
description: Assign or update assets in a project.
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
TQID: https://experienceleague.adobe.com/e1R0hBpDClLTqDXtiM2hEK1zujDE0XpexGhNoE56Dw8
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# setProjectAssets{#setprojectassets}

Assign or update assets in a project.

 Syntax 

## Authorized User Types {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Input (setProjectAssetsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyName  | `xsd:string`  | Yes  | Company handle.  |
|  projectHandle  | `xsd:string`  | Yes  | Project handle.  |
|  assetHandleArray  | `types:HandleArray`  | Yes  | The array of asset handles you want to associate with the project.  |

**Output (setProjectAssetsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  successCount  | `xsd:int`  | Yes  | The number of successfully added assets.  |

## Examples {#section-33c1a909c3dc4aa98da474c23a036596}

This code sample assigns an asset to a project. The request returns a success count of one.

**Request** 

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**Response** 

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```
