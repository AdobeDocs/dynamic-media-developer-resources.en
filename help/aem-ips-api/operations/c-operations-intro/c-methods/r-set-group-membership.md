---
description: Sets group membership for a user.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
TQID: 'https://experienceleague.adobe.com/j-wK2g-evSRY0YD3ZspgT--giCkKJl1VBYgPylixVz8'
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
# setGroupMembership{#setgroupmembership}

Sets group membership for a user.

 Syntax 

## Authorized User Types {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Input (setGroupMembershipParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  userHandle  | `xsd:string`  | No  | The handle to the user whose group membership you want to set.  |
|  companyHandle  | `xsd:string`  | No  | Company handle.  |
|  groupHandleArray  | `types:HandleArray`  | Yes  | The array of handles to groups to which the user to belongs.  |

**Output (setGroupMembershipReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-67b86d259df24938896fe19061845811}

This code sample makes the user a member of a group. Add a user to multiple groups with the group handle array.

**Request** 

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**Response**

None.
