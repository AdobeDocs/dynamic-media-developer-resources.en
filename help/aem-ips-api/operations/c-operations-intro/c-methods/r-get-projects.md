---
description: Gets projects for a group of related assets.
solution: Experience Manager
title: getProjects
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7262ed7-7419-4d6b-86ed-f3ad4657d654
TQID: 'https://experienceleague.adobe.com/8qz891-cE1hkh1ui-mY2AZIyBO7IWoklEmPXNXmUoUU'
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
# getProjects{#getprojects}

Gets projects for a group of related assets.

 Syntax 

## Authorized User Types {#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser` 
* `IpsAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-8d549237b8c440b4872a0a086ddc00a1}

**Input (getProjectsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company.  |

**Output (getProjectsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  projectArray  | `types:ProjectArray`  | Yes  | The array of projects associated with the company.  |

## Examples {#section-8b12d0b948f644f68bf9a16060d3849a}

This code sample returns all project handles in a project array.

**Request** 

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**Response** 

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```

