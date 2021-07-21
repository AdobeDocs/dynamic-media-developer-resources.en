---
description: Sets asset metadata using batch mode.
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
---
# batchSetAssetMetadata{#batchsetassetmetadata}

Sets asset metadata using batch mode.

 Syntax 

## Authorized User Types {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-7111ac93bc7747f69ba14db4ac3912b0}

**Input (batchSetAssetMetadataParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company whose metadata you want to set in a batch operation.  |
|  `*`updateArray`*`  | `types:BatchMetadataUpdateArray`  | Yes  | The array of metadata updates applied to the assets.  |

**Output (batchSetAssetMetadataParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`successCount`*`  | `xsd:int`  | Yes  | The number of successfully set metadata.  |
|  `*`warningCount`*`  | `xsd:int`  | Yes  | The number of warnings generated when the operation attempted to set metadata.  |
|  `*`errorCount`*`  | `xsd:int`  | Yes  | The number of errors generated when the operation attempted to set metadata.  |
|  `*`warningDetailArray`*`  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets generating warnings when the operation attempted to batch set metadata for the assets.  |
|  `*`errorDetailArray`*`  | `types:AssetOperationFaultArray`  | No  | The array of details associated with the assets that generating erros when the operation attempted to batch set metadata for the assets.  |

## Examples {#section-2de798ac920e4b47b971b1729a64395b}

**Request** 

```java
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**Response** 

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```
