---
description: Sets the thumbnail image for one or more assets.
seo-description: Sets the thumbnail image for one or more assets.
seo-title: batchSetThumbAsset
solution: Experience Manager
title: batchSetThumbAsset
uuid: 16c298a7-bb07-4643-824b-8f864d7f0290
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
---

# batchSetThumbAsset{#batchsetthumbasset}

Sets the thumbnail image for one or more assets.

 Syntax 

## Thumbnail Asset Types {#section-4edc2a6a8f824213b0aaddb1d437268c}

Allowed thumbnail asset types consist of the following:

* Image 
* AdjustedView 
* Mask 
* Template 
* PsdTemplate

## Authorized User Types {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read/write access to the target asset and read access to the thumb asset.

## Parameters {#section-9c6efa000b384b3db6c013def20cf40b}

**Input (batchSetThumbAssetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company that contains the assets.  |
|  `*`updateArray`*`  | `types:ThumbAssetUpdateArray`  | Yes  | The array of updates.  |

**Output (batchSetThumbAssetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`successCount`*`  | `xsd:int`  | Yes  | The number of successfully set thumbnails.  |
|  `*`warningCount`*`  | `xsd:int`  | Yes  | The number of warnings generated when the operation attempted to set the thumbnails.  |
|  `*`errorCount`*`  | `xsd:int`  | Yes  | The number of errors generated when the operation attempted to set the thumbnails.  |
|  `*`warningDetailArray`*`  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated warnings when the operation attempted to apply the updates.  |
|  `*`errorDetailArray`*`  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generated errors when the operation attempted to apply the updates.  |

## Examples {#section-6de69a8680c24c1486c5f01488393381}

**Request** 

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**Response** 

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```

