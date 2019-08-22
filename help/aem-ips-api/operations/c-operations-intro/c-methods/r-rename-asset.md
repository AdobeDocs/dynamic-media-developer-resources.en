---
description: Renames an asset.
seo-description: Renames an asset.
seo-title: renameAsset
solution: Experience Manager
title: renameAsset
topic: Scene7 Image Production System API
uuid: 953cabdb-9fa4-4b36-bf3b-707161f48974
index: y
internal: n
snippet: y
---

# renameAsset{#renameasset}

Renames an asset.

>[!NOTE]
>
>The `renameFiles` parameter has been deprecated for prior releases and removed from `renameAsset`. The virtual file path is changed to match the new asset name (preserving the file extension), while physical file paths are not affected. API clients need to remove references to this parameter when updating to the new API version.

## Authorized User Types {#section-cc27ad713c6d498b8f056850b20976f4}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImpagePortalContribUser`

>[!NOTE]
>
>The user must have read and write access to the asset.

## Parameters {#section-ef95a994106841e0ab346dd4cf672258}

**Input (renameAssetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company to which the asset belongs.  |
|  ` *`assetHandle`*`  | `xsd:string`  | Yes  | The handle to the asset you want to rename.  |
|  ` *`newName`*`  | `xsd:string`  | Yes  | Asset's new name.  |
|  ` *`validateName`*`  | `xsd:boolean`  | Yes  |If the `validateName` is `true` and the asset type requires a unique IPS ID, then the new name is checked for global uniqueness and `renameAsset` throws a fault if it is not unique.  |

**Output (renameAssetReturn)**

The IPS API does not return a response for this operation. See the description of the `<ns1:validateName>` element for caveats about this element.

## Examples {#section-a0ddffd62bec42e09069f22ceb486f8a}

This code sample renames an asset

**Request** 

```java
<ns1:renameAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:newName>My Newly Renamed Image</ns1:newName>
   <ns1:validateName>true</ns1:validateName>
   <ns1:renameFiles>true</ns1:renameFiles>
</ns1:renameAssetParam>
```

**Response**

None. 
