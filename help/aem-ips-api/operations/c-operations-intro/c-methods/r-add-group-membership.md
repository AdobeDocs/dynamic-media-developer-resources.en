---
description: Adds a user to an array of groups.
solution: Experience Manager
title: addGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c5b5e155-d285-4304-98bc-1d938793e2c0
TQID: 'https://experienceleague.adobe.com/E26D4T5xx58eE5G1APbIi46B-SL1BM9YqGibC1n4IVo'
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
# addGroupMembership{#addgroupmembership}

Adds a user to an array of groups.

 Syntax 

## Authorized User Types {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-e250f6ddb13646808c6a8860b6442bc5}

**Input (addGroupMembershipParam)** 

<table id="table_71AD8902E4854CA5A12379DBA4DF17C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Handle to the user whose group membership you want to add. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col4"> <p>Array of handles to the groups you want the company to belong to. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (addGroupMembershipParam)**

The IPS API does not return a response for this operation.

## Examples {#section-f7a1f40c3d7a40ea964b29056c734d81}

This example adds a group to a company with groupHandleArray. This example uses one group only.

**Request** 

```java {.line-numbers}
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Response**

None.
