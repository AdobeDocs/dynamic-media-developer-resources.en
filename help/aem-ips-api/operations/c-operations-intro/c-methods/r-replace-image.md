---
description: Replaces image data for an image asset.
seo-description: Replaces image data for an image asset.
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
topic: Scene7 Image Production System API
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
---

# replaceImage{#replaceimage}

Replaces image data for an image asset.

 Syntax 

## Authorized User Types {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Input (replaceImageParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyName`*`  | `xsd:string`  | Yes  | The handle to the company with the image you want to replace.  |
|  ` *`assetHandle`*`  | `xsd:string`  | Yes  | The handle to the asset you want to replace.  |
|  ` *`urlModifier`*`  | `xsd:string`  | Yes  | Image Server commands that generate new image data.  |

**Output (replaceImageReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`assetHandle`*`  | `xsd:string`  | Yes  | Handle to the new asset.  |

## Examples {#section-cebb93576bde4cb98cb27356ca66783b}

This code sample replaces an image and and applies a `urlModifier` with a command that specifies that the Image Server will take no action upon replacement.

**Request** 

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**Response** 

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```

