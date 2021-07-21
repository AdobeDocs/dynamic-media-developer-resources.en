---
description: Deletes an asset.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
---
# deleteAsset{#deleteasset}

Deletes an asset.

 Syntax 

## Authorized User Types {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read and delete access to the asset.

## Parameters {#section-0eed164e278b456fbdfb7a50727a0416}

**Input (deleteAssetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company to which the folder belongs.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | The handle to the asset to delete.  |

**Output (deleteAssetParam)**

The IPS API does not return a response for this operation.

## Examples {#section-d5657289f5234bb0a613dcf691507958}

This sample code deletes any type of asset from a specific company. It requires an asset handle, which you must obtain from another operation.

**Request** 

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Response**

None.
