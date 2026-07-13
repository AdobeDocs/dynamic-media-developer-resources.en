---
description: Deletes a project from a company. The links between the assets and the project are broken, but the assets are not deleted from IPS.
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
TQID: 'https://experienceleague.adobe.com/gZaX8EqLg3A4ca6EY9-xsFkz4HzWFbmLU2xsgU-LM-M'
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
# deleteProject{#deleteproject}

Deletes a project from a company. The links between the assets and the project are broken, but the assets are not deleted from IPS.

 Syntax 

## Authorized User Types {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-00d1e00dd5014513a52b4e6b4f61de62}

**Input (deleteProjectParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyName  | `xsd:string`  | Yes  | The name of the company associated with the project.  |
|  projectHandle  | `xsd:string`  | Yes  | The handle to the project to be deleted.  |

**Output (deleteProjectReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-e38507f1f7ec41b9a625f47390490254}

This code sample uses the company handle and the project handle as fields in the deleteProjectParam sent to the IPS Web services server in order to delete the project.

**Request** 

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Response**

None.

