---
description: Deletes an image map.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
TQID: 'https://experienceleague.adobe.com/6r-EiZLM0tRUpzoTJyTt3rAkyABfNH9DQvDJq-XsqPY'
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
# deleteImageMap{#deleteimagemap}

Deletes an image map.

 Syntax 

## Authorized User Types {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>The user must have read and write access to the asset.

## Parameters {#section-28de12bab79045a5977c68855e37ae3d}

**Input (deleteImageMapParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company that contains the image map to delete.  |
|  imageMapHandle  | `xsd:string`  | Yes  | The handle to the image map to delete.  |

**Output (deleteImageMapParam)**

The IPS API does not return a response for this operation.

## Examples {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

This code sample deletes an image map from a company. You must obtain the image map handle from another operation.

**Request** 

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Response**

None

