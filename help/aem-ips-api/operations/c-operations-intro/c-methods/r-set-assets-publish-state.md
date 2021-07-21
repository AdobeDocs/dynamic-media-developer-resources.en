---
description: Determines if a batch of assets are ready to be published.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
---
# setAssetsPublishState{#setassetspublishstate}

Determines if a batch of assets are ready to be published.

 This is the batch version of [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563). 

## Authorized User Types {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read and write access to the asset.

## Parameters {#section-3e49d7859f8647b990d75373cc8dbc24}

**Input (setAssetsPublishStateParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | Company handle.  |
|  `*`publishStateUpdateArray`*`  | `types:PublishStateUpdateArray`  | Yes  | Array of publish state values for the assets.  |

**Output (setAssetsPublishStateParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`successCount`*`  | `xsd:int`  | Yes  | The number of successfully updated assets.  |
|  `*`warningCount`*`  | `xsd:int`  | Yes  | The number of assets that generated a warning when the operation tried to update them.  |
|  `*`errorCount`*`  | `xsd:int`  | Yes  | The number of assets that generated an error when the operation tried to delete them.  |
|  `*`warningDetailArray`*`  | `types:AssetOperationFaultArray`  | No  | Details associated with the asset updates that generated a warning.  |
|  `*`errorDetailArray`*`  | `types:AssetOperationFaultArray`  | No  | Details associated with the asset updates that generated an error.  |

## Examples {#section-38cfdd3436214a06a1bae16875501d51}

This code sample sets the publication state of an asset.

**Request** 

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**Response** 

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```
