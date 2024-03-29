---
description: Deletes a current or scheduled job.
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
---
# deleteJob{#deletejob}

Deletes a current or scheduled job.

 Syntax 

## Authorized User Types {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-000c42bc93744b1a8e777f3ec3c272b0}

**Input (deleteJobParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company to which the job belongs.  |
|  jobHandle  | `xsd:string`  | Yes  | The handle to the job to delete.  |

**Output**

The IPS API does not return a response for this operation.

## Examples {#section-732d21d4dad04337b7a5ae1a0cc00eba}

This code sample deletes a job that is running or is scheduled to run in IPS. It requires a job handle, which you must obtain from another operation.

**Request** 

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Response**

None.
