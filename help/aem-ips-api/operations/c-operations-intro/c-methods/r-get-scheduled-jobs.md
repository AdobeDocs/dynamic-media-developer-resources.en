---
description: Gets jobs scheduled to run.
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
TQID: 'https://experienceleague.adobe.com/DNUaAhcCeO8MvLH5YF5-WTA74fCyRKLxvXBKu0ltngk'
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
# getScheduledJobs{#getscheduledjobs}

Gets jobs scheduled to run.

 Syntax 

## Authorized User Types {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-2af604ff8282460990b9237158187f8f}

**Input (getScheduledJobsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company.  |
|  jobHandle  | `xsd:string`  | No  | Job handle.  |
|  originalName  | `xsd:string`  | No  |The name specified by `submitJob`.  |

**Output (getScheduledJobsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  jobArray  | `types:ScheduledJobArray`  | Yes  | Array of scheduled jobs.  |

## Examples {#section-e79e7da86ba848fd9996aa36de462e6c}

This code sample returns all scheduled jobs in a job array. The array itself contains detailed information about the jobs.

**Request** 

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**Response** 

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```
