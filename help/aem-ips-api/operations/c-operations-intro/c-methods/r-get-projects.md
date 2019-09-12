---
description: Gets projects for a group of related assets.
seo-description: Gets projects for a group of related assets.
seo-title: getProjects
solution: Experience Manager
title: getProjects
topic: Scene7 Image Production System API
uuid: 46ec9a5d-4414-4c9c-aaf2-0db654204b61
index: y
internal: n
snippet: y
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
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company.  |

**Output (getProjectsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`projectArray`*`  | `types:ProjectArray`  | Yes  | The array of projects associated with the company.  |

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

