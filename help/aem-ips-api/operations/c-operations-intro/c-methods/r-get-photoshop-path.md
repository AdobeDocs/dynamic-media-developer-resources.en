---
description: Returns coordinates for the quadrilateral enclosing the named Photoshop path.
solution: Experience Manager
title: getPhotoshopPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 46d88547-bb60-4370-9c79-bd281b40ba28
TQID: https://experienceleague.adobe.com/GldZWrxFuEcANPrpPo6TvZjZ6jHElZt7u6W7gzmbsFg
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# getPhotoshopPath{#getphotoshoppath}

Returns coordinates for the quadrilateral enclosing the named Photoshop path.

 Syntax 

## Authorized User Types {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `IpsUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser` 
* ``

## Parameters {#section-ebffe496284c4ced9f329f78127be199}

**Input (getPhotoshopPathParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | Handle to the company with the image you want to work with.  |
|  assetHandle  | `xsd:string`  | Yes  | Handle to the image asset.  |
|  pathName  | `xsd:string`  | Yes  | Name of the Photoshop path you want to return.  |

**Output (getPhotoshopPathReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  perspectiveQuad  | `types:PerspectiveQuad`  | Yes  |Returns image coordinates based on the path. See [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204).  |

## Examples {#section-1f0461cbdc184c8d8925336d5279db47}

**Request** 

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**Response** 

```java
<getPhotoshopPathReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <perspectiveQuad>
    <x0>932.19</x0>
    <y0>296.592</y0>
    <x1>968.769</x1>
    <y1>320.16</y1>
    <x2>1119.56</x2>
    <y2>1200.0</y2>
    <x3>900.43</x3>
    <y3>1200.0</y3>
  </perspectiveQuad>
</getPhotoshopPathReturn>
```

>[!MORELIKETHIS]
>
>* [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)
