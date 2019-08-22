---
description: Sets metadata values for an asset. Works with an array of metadata updates to set values in a batch.
seo-description: Sets metadata values for an asset. Works with an array of metadata updates to set values in a batch.
seo-title: setAssetMetadata
solution: Experience Manager
title: setAssetMetadata
topic: Scene7 Image Production System API
uuid: f91bfb5d-6493-4d53-9ea5-b4c7f9794e56
index: y
internal: n
snippet: y
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
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company with the asset you want to update.  |
|  ` *`assetHandle`*`  | `xsd:string`  | Yes  | The handle to the asset.  |
|  ` *`updateArray`*`  | `types:MetadataUpdateArray`  | Yes  | Updates in a metadata update array.  |

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
