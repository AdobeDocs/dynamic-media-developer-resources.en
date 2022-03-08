---
description: Restarts a paused job.
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
---
# resumeJob{#resumejob}

Restarts a paused job.

 Syntax 

## Authorized User Types {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**Input (resumeJobParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company with the job you want to restart.  |
|  jobHandle  | `xsd:string`  | Yes  | The handle to the paused job.  |

**Output (resumeJobReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-d0524e031f1f43d89430eade19526162}

This code sample restarts a paused job.

**Request** 

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**Response**

None.
