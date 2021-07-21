---
description: Returns all metadata fields, grouped by asset type.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
---
# getAssetMetadataFields{#getassetmetadatafields}

Returns all metadata fields, grouped by asset type.

 Syntax 

## Authorized User Types {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**Input (getAssetMetadataFieldsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company whose metadata you want to retrieve.  |

**Output (getAssetMetadataFieldsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`assetFieldArray`*`  | `types:AssetMetadataFieldsArray`  | Yes  | Array of metadata fields, by asset type.  |

## Examples {#section-d79ab85f29144635b0b61416e52f4f3f}

**Request** 

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**Response** 

>[!NOTE]
>
>Truncated for brevity.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
