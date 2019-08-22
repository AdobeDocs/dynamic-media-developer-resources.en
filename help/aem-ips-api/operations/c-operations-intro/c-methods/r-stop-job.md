---
description: Stops a job in progress.
seo-description: Stops a job in progress.
seo-title: stopJob
solution: Experience Manager
title: stopJob
topic: Scene7 Image Production System API
uuid: 5e1ebafa-acce-4894-80b1-7b931bb39025
index: y
internal: n
snippet: y
---

# stopJob{#stopjob}

Stops a job in progress.

 Syntax 

## Authorized User Types {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-2b64f074e37c4c38849994f3bc65342a}

**Input (stopJobParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | Company handle.  |
|  ` *`jobHandle`*`  | `xsd:string`  | Yes  | Handle to the job you want to stop.  |

**Output (stopJobReturn0**

The IPS API does not return a response for this operation.

## Examples {#section-f7e07fa09ae24dc89685533f20ab3b81}

**Request** 

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**Response**

None. 
