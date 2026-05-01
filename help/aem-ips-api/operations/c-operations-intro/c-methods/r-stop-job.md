---
description: Stops a job in progress.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
TQID: https://experienceleague.adobe.com/nOMGgTqTuVQAssNzqvxANf-kvPP-ZjkjzN-dymAiV8M
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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
|  companyHandle  | `xsd:string`  | Yes  | Company handle.  |
|  jobHandle  | `xsd:string`  | Yes  | Handle to the job you want to stop.  |

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
