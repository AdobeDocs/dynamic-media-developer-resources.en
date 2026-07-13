---
description: Renames a project.
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
TQID: 'https://experienceleague.adobe.com/FjPL1Xn4QAYYCdyeYKA1MiQVay988g-sbuiHpazhcMM'
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
# renameProject{#renameproject}

Renames a project.

 Syntax 

## Authorized User Types {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-43ccd77648784be4a259a723c3e1db40}

**Input (renameProjectParam)**

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyName  | `xsd:string`  | Yes  | Handle to the company with the project you want to rename.  |
|  projectHandle  | `xsd:string`  | Yes  | Handle to the project.  |
|  projectName  | `xsd:string`  | Yes  | New project name.  |

**Output (renameProjectParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  projectHandle  | `xsd:string`  | Yes  | The handle of the renamed project.  |

## Examples {#section-a0a06d9244774795b695a10b92b2a5e7}

This code sample renames a project and returns the project handle.

**Request** 

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**Response** 

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```

