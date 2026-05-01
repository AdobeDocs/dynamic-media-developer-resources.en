---
description: Creates a new project.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
TQID: https://experienceleague.adobe.com/-h4FDOUNPjLA2L7qqmjfx8jVs2eJ5egOJxHBTivJqWE
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# createProject{#createproject}

Creates a new project.

 Syntax 

## Authorized User Types {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-8c741884eb54489bbaad0c444fee80b6}

**Input (createProjectParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle of the company associated with the new project.  |
|  projectName  | `xsd:string`  | Yes  | New project name.  |

**Output (createProjectParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  projectHandle  | `xsd:string`  | Yes  | The handle to the new project.  |

## Examples {#section-a0cd532b67e346d088fbec141231a0e5}

This code sample creates a project called `ApiTestProject` in a company specified by its handle. The response returns the handle to the project.

**Request** 

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>

```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```
