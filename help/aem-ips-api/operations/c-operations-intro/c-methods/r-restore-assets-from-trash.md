---
description: Restores assets from trash.
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b1cde1a9-d726-4ebc-9d49-ee72a6b56fc9
TQID: 'https://experienceleague.adobe.com/VeC7td4UAm7HX4azZATUoBf-ZLS00aF7OOipZqmVbdw'
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
# restoreAssetsFromTrash{#restoreassetsfromtrash}

Restores assets from trash.

 Syntax 

## Authorized User Types {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-200a61d040c94e489a85241b29cd499a}

**Input (restoreAssetsFromTrashParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to a company with the assets you want to restore.  |
|  assetHandleArray  | `types:HandleArray`  | Yes  | Array of handles for the assets you want to restore.  |

**Output (restoreAssetsFromTrashReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  successCount  | `xsd:int`  | Yes  | Number of assets successfully removed from the trash.  |
|  warningCount  | `xsd:int`  | Yes  | Number of warnings generated when the operation attempted to restore assets from the trash.  |
|  errorCount  | `xsd:int`  | Yes  | Number of errors generated when attempting to restore assets from the trash.  |
|  warningDetailArray  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated warnings when the operation attempted to restore assets from the trash.  |
|  errorDetailArray  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated errors when the operation attempted to restore assets from the trash.  |

## Examples {#section-98fe0394b0634ca397c395f14f8a9358}

This code sample restores assets from the trash. The response indicates the operation completed successfully.

**Request** 

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**Response** 

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```
