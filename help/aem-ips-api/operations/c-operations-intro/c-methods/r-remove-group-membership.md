---
description: Removes users from an array of groups.
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 892ee01c-e07b-4321-b0b7-5bb606036340
TQID: 'https://experienceleague.adobe.com/-RTuwtlTpQdiS-H-lf9BhQwbkp5McXo4tbxssF-0wzo'
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
# removeGroupMembership{#removegroupmembership}

Removes users from an array of groups.

 **Differences Between Remove Commands**

* `removeGroupMembers`: Removes multiple users from a group. 
* `removeGroupMembership`: Removes an individual user from an array of groups.

## Authorized User Types {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Input (removeGroupMembershipParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  userHandle  | `xsd:string`  | No  | The handle to the company whose group membership you want to remove.  |
|  groupHandleArray  | `types:HandleArray`  | Yes  | The array of handles to groups from which you want the company to be removed.  |

**Output (removeGroupMembershipReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-f8d4181170a243efb9faf5824ae96197}

This code sample removes a user from a group.

**Request** 

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**Response**

None.

