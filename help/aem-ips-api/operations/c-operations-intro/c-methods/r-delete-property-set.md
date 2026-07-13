---
description: Deletes a property set and all associated properties.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
TQID: 'https://experienceleague.adobe.com/1j45J5Kw5P-3ba3WLNy9sTDBC5g4L17bynJQRaU5lAM'
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
# deletePropertySet{#deletepropertyset}

Deletes a property set and all associated properties.

 Syntax 

## Authorized User Types {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-e5fc868f69494cf6858e03027db09101}

**Input (deletePropertySetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  setHandle  | `xsd:string`  | Yes  | The handle to the property set to be deleted.  |

**Output (deletePropertySetParam)**

The IPS API does not return a response for this operation.

## Examples {#section-cf319fc8f86a40ab9cbd838b031973fe}

This code sample uses the set’s handle as a field in the `deletePropertySetParam` sent to the IPS Web services server in order to delete the property set.

**Request** 

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Response**

None.

