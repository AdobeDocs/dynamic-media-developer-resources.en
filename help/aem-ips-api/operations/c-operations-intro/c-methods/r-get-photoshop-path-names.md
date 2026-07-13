---
description: Returns an array of Photoshop path names for the given image.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
TQID: 'https://experienceleague.adobe.com/BxFBNXpa9ilc4lXeXiuuvCQb9ChImZWt13-pJ3b3osk'
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
# getPhotoshopPathNames{#getphotoshoppathnames}

Returns an array of Photoshop path names for the given image.

 Syntax 

## Authorized User Types {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `IpsUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-605a4aab23104489a21f7f7f5849801b}

**Input (getPhotoshopPathNamesParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | Handle to the company that contains the image you want to work with.  |
|  assetHandle  | `xsd:string`  | Yes  | Handle to the image asset.  |

**Output (getPhotoshopPathNamesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  pathNameArray  | `types:StringArray`  | Yes  | An array of Photoshop path names in an image.  |

## Examples {#section-6d316f14b4184d42af4ca3f717b042dd}

**Request** 

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**Response** 

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```

