---
description: Creates a new project.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
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
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle of the company associated with the new project.  |
|  `*`projectName`*`  | `xsd:string`  | Yes  | New project name.  |

**Output (createProjectParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`projectHandle`*`  | `xsd:string`  | Yes  | The handle to the new project.  |

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

