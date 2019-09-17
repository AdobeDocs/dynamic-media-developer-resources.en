---
description: Updates an asset set.
seo-description: Updates an asset set.
seo-title: updateAssetSet
solution: Experience Manager
title: updateAssetSet
topic: Scene7 Image Production System API
uuid: e844a395-0ab3-45a7-bcec-8e9e15efc70e
---

# updateAssetSet{#updateassetset}

Updates an asset set.

 Syntax 

## Parameters {#section-d7080ccd97334c94860eb107a3e132b2}

**Input (updateAssetSetParam)**

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company that contains the image set you want to modify.  |
|  ` *`assetHandle`*`  | `xsd:string`  | Yes  | The handle to the image set you want to modify.  |
|  ` *`setDefinition`*`  | `xsd:string`  | No  | Resets image set members.  |
|  ` *`thumbAssetHandle`*`  | `xsd:string`  | No  | The handle of the asset that acts as the thumbnail for the image set.  |

**Output (updateAssetSetReturn)**

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|   |  |  |  |

## Examples {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Request** 

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**Response** 

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

