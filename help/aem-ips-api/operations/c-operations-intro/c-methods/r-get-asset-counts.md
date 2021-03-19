---
description: Gets the assets and the number of assets associated with a specific company.
seo-description: Gets the assets and the number of assets associated with a specific company.
seo-title: getAssetCounts
solution: Experience Manager
title: getAssetCounts
uuid: 92103806-59da-444f-b69c-d045d0ebf42e
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
---

# getAssetCounts{#getassetcounts}

Gets the assets and the number of assets associated with a specific company.

The `countArray` returned consists of an array of `assetTypes` (data type `xsd:string`), each with its own count field (data type `xsd:int`), allowing the representation of multiple asset types per element of the array. 
Syntax 

## Authorized User Types {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**Input (getAssetCountsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company with assets you want to count.  |

**Output (getAssetCountsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`countArray`*`  | `types:AssetCountArray`  | No  | An array of asset types, each with its own count field, allowing the representation of multiple asset types per element of the array.  |

## Examples {#section-6052a503eb3843f6adb99e200fdba280}

This code sample uses the company’s handle as a field in the `getAssetCountsParam` sent to the IPS Web services server in order to get the asset counts.

**Request** 

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**Response** 

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```

