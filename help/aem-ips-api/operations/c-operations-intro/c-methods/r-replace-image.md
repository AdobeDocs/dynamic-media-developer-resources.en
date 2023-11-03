---
description: Replaces image data for an image asset.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
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
|  companyName  | `xsd:string`  | Yes  | The handle to the company with the image you want to replace.  |
|  assetHandle  | `xsd:string`  | Yes  | The handle to the asset you want to replace.  |
|  urlModifier  | `xsd:string`  | Yes  | Image Server commands that generate new image data.  |

**Output (replaceImageReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  assetHandle  | `xsd:string`  | Yes  | Handle to the new asset.  |

## Examples {#section-cebb93576bde4cb98cb27356ca66783b}

This code sample replaces an image and applies a `urlModifier` with a command that specifies that the Image Server take no action on replacement.

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
