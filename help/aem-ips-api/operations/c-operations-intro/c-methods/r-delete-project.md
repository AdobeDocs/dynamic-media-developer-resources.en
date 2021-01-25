---
description: Deletes a project from a company. The links between the assets and the project are broken, but the assets are not deleted from IPS.
seo-description: Deletes a project from a company. The links between the assets and the project are broken, but the assets are not deleted from IPS.
seo-title: deleteProject
solution: Experience Manager
title: deleteProject
topic: Dynamic Media Image Production System API
uuid: 0915066f-2106-4cbc-a68a-f149810c24f8
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
|  `*`companyName`*`  | `xsd:string`  | Yes  | The name of the company associated with the project.  |
|  `*`projectHandle`*`  | `xsd:string`  | Yes  | The handle to the project to be deleted.  |

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
