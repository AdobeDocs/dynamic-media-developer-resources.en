---
description: Deletes a company's metadata field.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
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
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company that contains the metadata field to be deleted.  |
|  `*`fieldHandle`*`  | `xsd:string`  | Yes  | The handle to the metadata field to be deleted.  |

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
