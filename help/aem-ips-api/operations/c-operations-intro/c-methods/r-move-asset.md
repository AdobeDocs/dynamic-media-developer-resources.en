---
description: Moves an asset to a specific folder.


solution: Experience Manager
title: moveAsset

feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
---

# moveAsset{#moveasset}

Moves an asset to a specific folder.

 Syntax 

## Authorized User Types {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-dd0bbdf293aa4563af70a91f97c861f1}

**Input (moveAssetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | Handle to the company.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | Handle to the asset you want to move.  |
|  `*`folderHandle`*`  | `xsd:string`  | Yes  | Handle to the destination folder.  |

**Output (moveAssetReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-78333769f4f14e2886fdf06433c9d2ad}

This code sample moves an asset to a folder.

**Request** 

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**Response**

None. 
