---
description: Creates a new asset derived from an existing primary source image asset.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
---
# createDerivedAsset{#createderivedasset}

Creates a new asset derived from an existing primary source image asset.

 Syntax 

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Derived assets specify Image Server protocol commands that modify the representation of the owner image. The `AdjustedView` derived type helps apply simple modifications to a single image (for example, by specifying a crop rectangle), while the `LayerView` helps create a multilayer view which may include text or additional images.

Unlike an image copy (see [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), a derived image is linked to its owner image. Changes to the owner image modifies associated derived assets. Deleting the owner image will delete any associated derived images.

## Authorized User Types {#authorized-user-types}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-5a0dde01cff6454da3646ea805c2be1e}

**Input (createDerivedAssetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company that contains the asset from which you will derive the new asset.  |
|  `*`ownerHandle`*`  | `xsd:string`  | Yes  | The handle to the primary Image asset from which the new image will be derived.  |
|  `*`folderHandle`*`  | `xsd:string`  | Yes  | The handle to the folder in which the new derived asset will be created.  |
|  `*`name`*`  | `xsd:string`  | Yes  | The name of the derived asset.  |
|  `*`type`*`  | `xsd:string`  | Yes  |The asset type of the new derived asset: `AdjustedView` or `LayerView`.  |
|  `*`urlModifier`*`  | `xsd:string`  | No  |Image serving or image rendering protocol commands applied *before* the request or `urlPostApplyModifier` commands.  |
|  `*`urlPostApplyModifier`*`  | `xsd:string`  | No  |Image serving or image rendering protocol commands applied *after* to the request or `urlPostApplyModifier` commands.  |

**Output (createDerivedAssetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | The handle to the derived asset.  |

## Examples {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

The sample code creates a derived asset with an adjusted view and `urlModifier` and `urlPostApplyModifier` with arbitrary values. The response returns the handle to the newly derived asset.

**Request** 

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**Response** 

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```
