---
description: Pauses an active job.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
TQID: 'https://experienceleague.adobe.com/7zMJW9fm8DiAPrO5cCDl87FhFMbgpw5NxoBHmIfEBog'
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
# pauseJob{#pausejob}

Pauses an active job.

 Syntax 

## Authorized User Types {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-7aedb924cf8b4e05a0dc927636d537a0}

**Input (pauseJobParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | Handle to the company.  |
|  jobHandle  | `xsd:string`  | Yes  | Handle to the job you want to pause.  |

**Output (PauseJobReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-ee4914f9496f4bd88556728a48fb22c1}

This code sample pauses an active job.

**Request** 

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**Response**

None.

