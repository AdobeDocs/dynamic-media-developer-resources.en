---
description: Returns image formats, such as PDF, EPS, SWF, and others.
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
TQID: https://experienceleague.adobe.com/rATVnj3WwoHVGct-q3SonAhR95ggPQxfhj7ezJwFdw0
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# getImageFormats{#getimageformats}

Returns image formats, such as PDF, EPS, SWF, and others.

 Syntax 

## Authorized User Types {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser` 
* `IspAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-eefa36a70b74498f8727ef61d98cfb63}

**Input (getImageFormatsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company with the image formats you want to obtain.  |

**Output (getImageFormatsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  imageFormatArray  | `types:ImageFormatArray`  | Yes  | The image format array.  |

## Examples {#section-73881e12839b4904bf3299b0920bdd0c}

This code sample returns all image formats for the specified company.

**Request** 

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**Response** 

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```
