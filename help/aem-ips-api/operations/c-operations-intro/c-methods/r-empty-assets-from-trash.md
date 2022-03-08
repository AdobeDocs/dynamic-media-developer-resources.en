---
title: emptyAssetsFromTrash
description: Empties assets from the IPS trash.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
---
# emptyAssetsFromTrash{#emptyassetsfromtrash}

Empties assets from the IPS trash.

Assets live in the trash until they are manually emptied or until they time out of the trash. If they are manually emptied, they live in the Trash until the next cleanup job (normally nightly) when they are finally purged from the system. If they time out of the trash, assets are cleaned off as part of that same cleanup activity. The time out is configurable (defaults is 7 days).

## Authorized User Types {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser` 

## Parameters {#section-8e1fb0ee3aae453581e99ef76e298569}

**Input (emptyAssetsFromTrashParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | xsd:string  | Yes  | The handle to the company that owns the assets.  |
|  assetHandleArray  | types:HandleArray  | Yes  | The array of handles that represent the items to be emptied from the trash.  |

**Output (emptyAssetsFromTrashParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  successCount  | xsd:Int  | Yes  | The number of assets successfully emptied from the trash.  |
|  warningCount  | xsd:Int  | Yes  | The number of warnings generated when the operation attempted to empty assets from the trash.  |
|  errorCount  | xsd:Int  | Yes  | The number of errors generated when the operation attempted to empty assets from the trash.  |
|  warningDetailArray  | types:AssetOperationFaultArray  | No  | The array of details associated with the assets that generated warnings when the operation attempted to empty them from the trash.  |
|  errorDetailArray  | types:AssetOperationFaultArray  | No  | The array of details associated with the assets that generated errors when the operation attempted to empty them from the trash.  |

## Examples {#section-6154a873b6c342bf92e2036280cafdcf}

This code sample uses the company’s handle and an asset handle array that contains handles to the assets to be emptied from the trash.

**Request** 

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Response** 

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
