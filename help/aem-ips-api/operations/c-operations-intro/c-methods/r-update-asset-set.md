---
description: Updates an asset set.
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
TQID: https://experienceleague.adobe.com/Htyl1u04XqYmxWrUfb5wfiBtRjs07e57wGY7rR1YUjM
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# updateAssetSet{#updateassetset}

Updates an asset set.

 Syntax 

## Parameters {#section-d7080ccd97334c94860eb107a3e132b2}

**Input (updateAssetSetParam)**

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company that contains the image set you want to modify.  |
|  assetHandle  | `xsd:string`  | Yes  | The handle to the image set you want to modify.  |
|  setDefinition  | `xsd:string`  | No  | Resets image set members.  |
|  thumbAssetHandle  | `xsd:string`  | No  | The handle of the asset that acts as the thumbnail for the image set.  |

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
