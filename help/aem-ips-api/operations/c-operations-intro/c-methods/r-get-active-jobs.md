---
description: Gets all currently active jobs.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
TQID: 'https://experienceleague.adobe.com/YTwzh2h9wVPuURKL5nNFoac2SruwYXDw9oWtd-vzowc'
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
|  companyHandle  | `xsd:string`  | No  | The handle to the company.  |
|  jobHandle  | `xsd:string`  | No  | The handle to the job.  |
|  originalName  | `xsd:string`  | No  | Original job name.  |

**Output (getActiveJobsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  jobArray  | `xsd:string`  | Yes  | Array of active jobs.  |

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
