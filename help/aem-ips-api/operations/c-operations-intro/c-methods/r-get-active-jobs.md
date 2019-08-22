---
description: Gets all currently active jobs.
seo-description: Gets all currently active jobs.
seo-title: getActiveJobs
solution: Experience Manager
title: getActiveJobs
topic: Scene7 Image Production System API
uuid: 31edd0d1-3f7c-4d50-b137-094e9862d94a
index: y
internal: n
snippet: y
---

# getActiveJobs{#getactivejobs}

Gets all currently active jobs.

 Syntax 

## Authorized User Types {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**Input (getActiveJobsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | No  | The handle to the company.  |
|  ` *`jobHandle`*`  | `xsd:string`  | No  | The handle to the job.  |
|  ` *`originalName`*`  | `xsd:string`  | No  | Original job name.  |

**Output (getActiveJobsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`jobArray`*`  | `xsd:string`  | Yes  | Array of active jobs.  |

## Examples {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

This code sample returns all active jobs of a company running in IPS. In this case, the response is unusual because the IPS scheduling coordinator is disabled with no active jobs running. Under normal circumstances, the response would return a number of active jobs.

**Request** 

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**Response** 

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```
