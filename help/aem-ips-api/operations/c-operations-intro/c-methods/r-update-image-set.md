---
description: Updates an image set.
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
---
# updateImageSet{#updateimageset}

Updates an image set.

 Syntax 

## Parameters {#section-3be47dbbce474ce78676b05e163492e3}

**Input (updateImageSetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company that contains the image set you want to modify.  |
|  assetHandle  | `xsd:string`  | Ys  | The handle to the image set you want to modify.  |
|  memberArray  | `types:ImageSetMemberUpdateArray`  | No  | Resets image set members.  |
|  thumbAssetHandle  | `xsd:string`  | No  | The handle of the asset that acts as the thumbnail for the image set.  |

**Output (updateImageSetReturn)**

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  sequence  |  |  |  |

## Examples {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Request** 

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**Response** 

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```
