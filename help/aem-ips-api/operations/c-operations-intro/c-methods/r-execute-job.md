---
description: Runs a specific job.
solution: Experience Manager
title: executeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4b2a2a14-d785-43bd-b1fc-2812d9f21964
TQID: 'https://experienceleague.adobe.com/CEj3hHL2AKEviGPPmEZy6LyX0thhqKKFBQfdxK82r6w'
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
# executeJob{#executejob}

Runs a specific job.

 Syntax 

## Authorized User Types {#section-8199e8599ea64e7097a2acb633417b15}

* `IpsUser` 
* `IpsAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-2c61b2bffcf9479a9391f2c13fdf7d53}

**Input (executeJobParam)**

<table id="table_FA410513908F4084A21A5F0A9431006C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Required </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col4"> <p>The handle to the company to which the job belongs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> jobHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col4"> <p>The handle to the job to run. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (executeJobReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-96f71aa58a954293b9a98ff96d86f232}

This code sample runs a job that is scheduled to run in IPS.

**Request**

```java
<executeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</executeJobParam>
```

**Response**

None.

