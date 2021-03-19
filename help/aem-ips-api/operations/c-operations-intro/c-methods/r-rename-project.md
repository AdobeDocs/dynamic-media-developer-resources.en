---
description: Renames a project.
seo-description: Renames a project.
seo-title: renameProject
solution: Experience Manager
title: renameProject
uuid: 6303c493-a6fe-4b32-80c3-947aba4190f7
feature: "Dynamic Media Classic,SDK/API,Asset Management"
role: "Developer,Administrator"
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
|  `*`companyName`*`  | `xsd:string`  | Yes  | Handle to the company with the project you want to rename.  |
|  `*`projectHandle`*`  | `xsd:string`  | Yes  | Handle to the project.  |
|  `*`projectName`*`  | `xsd:string`  | Yes  | New project name.  |

**Output (renameProjectParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`projectHandle`*`  | `xsd:string`  | Yes  | The handle of the renamed project.  |

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

