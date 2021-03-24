---
description: Gets a list of active publish contexts for the specified company. A publish context is considered active if there is at least one active server defined for the context.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# getActivePublishContext{#getactivepublishcontext}

Gets a list of active publish contexts for the specified company. A publish context is considered active if there is at least one active server defined for the context.

 Syntax 

## Authorized User Types {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-a4be4024e55c472fa6728faec9c5e048}

**Input (getActivePublishContextsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company to query for active publish contexts  |

**Output (getActivePublishContextsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`contextArray`*`  | `types:StringArray`  | Yes  | The array of active publish contexts, which may include zero or more values from Publish Context.  |

