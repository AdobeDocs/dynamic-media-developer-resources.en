---
description: Replaces image data for an image asset.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
TQID: 'https://experienceleague.adobe.com/11bWPLId2s4gOVhiIFr93Ca4D-7SJ0PYHFmiSKtStjk'
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

