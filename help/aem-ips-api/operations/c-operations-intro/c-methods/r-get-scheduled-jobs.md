---
description: Gets jobs scheduled to run.


solution: Experience Manager
title: getScheduledJobs

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
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
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company.  |
|  `*`jobHandle`*`  | `xsd:string`  | No  | Job handle.  |
|  `*`originalName`*`  | `xsd:string`  | No  |The name specified by `submitJob`.  |

**Output (getScheduledJobsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`jobArray`*`  | `types:ScheduledJobArray`  | Yes  | Array of scheduled jobs.  |

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

