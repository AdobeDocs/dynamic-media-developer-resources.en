---
description: Deletes a company's metadata field.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
TQID: 'https://experienceleague.adobe.com/GnKkb-vTCdD5PwU111sxefzxR7FN74hk3i66c3gcH9I'
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
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
---
# deleteMetadataField{#deletemetadatafield}

Deletes a company's metadata field.

 Syntax 

## Authorized User Types {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-73f12a30cc4340b6b32dd11effd5195e}

**Input (deleteMetadataFieldParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company that contains the metadata field to be deleted.  |
|  fieldHandle  | `xsd:string`  | Yes  | The handle to the metadata field to be deleted.  |

**Output (deleteMetadataFieldParam)**

The IPS API does not return a response for this operation.

## Examples {#section-e1c474ea91a040609ecd7c2400f4fa3c}

This code sample deletes a company's metadata field. It uses the company handle and metadata handle as fields in the `deleteMetadataFieldParam` passed in to the IPS Web services server to perform this action.

**Request** 

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Response**

None.0

