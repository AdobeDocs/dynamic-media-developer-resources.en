---
description: Sets the group membership of users that belong to a specific company.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
TQID: 'https://experienceleague.adobe.com/9gCJ-UKUNZI3AbQ0LFkxNUSS-w7bnG0FQE8SQeM2MMQ'
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
# setGroupMembers{#setgroupmembers}

Sets the group membership of users that belong to a specific company.

 The operation throws an authentication fault if you do not have privileges to accomplish this operation. This is also true if any of the users in the user handle array do not belong to the company specified in the company handle, 

## Authorized User Types {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-6a18562fc8e942af94be10bbb8c51151}

**Input (setGroupMembersParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | Company handle.  |
|  groupHandle  | `xsd:string`  | Yes  | Group handle.  |
|  userHandleArray  | `types:HandleArray`  | Yes  | Array of handles for users whose group membership you want to set.  |

**Output (setGroupMembesReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-9c528c3f44a141ce9eaddf634f26c487}

This code sample sets group membership for a single user.

**Request** 

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**Response**

None.

