---
description: Sets metadata values for an asset. Works with an array of metadata updates to set values in a batch.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
TQID: 'https://experienceleague.adobe.com/b8E8BK8pyJQiYlR2yNMbYPWcLVNfmAvI5WaOBuaBz1E'
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
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
---
# setAssetMetadata{#setassetmetadata}

Sets metadata values for an asset. Works with an array of metadata updates to set values in a batch.

 Syntax 

## Authorized User Types {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read access to the asset.

## Parameters {#section-bcdcff30905e444388811e897b2824bd}

**Input (setAssetMetadataParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company with the asset you want to update.  |
|  assetHandle  | `xsd:string`  | Yes  | The handle to the asset.  |
|  updateArray  | `types:MetadataUpdateArray`  | Yes  | Updates in a metadata update array.  |

**Output (setAssetMetadataReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-1ab412e7ee1d4d6d8469b0b403598c42}

This code sample uses an array of metadata updates to set the metadata of the specified asset.

**Request** 

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**Response**

None.
