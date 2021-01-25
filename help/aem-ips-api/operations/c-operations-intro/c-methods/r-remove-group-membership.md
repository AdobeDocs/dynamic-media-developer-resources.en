---
description: Removes users from an array of groups.
seo-description: Removes users from an array of groups.
seo-title: removeGroupMembership
solution: Experience Manager
title: removeGroupMembership
topic: Dynamic Media Image Production System API
uuid: 553d91a3-73d6-4323-9436-a3ba13260a6c
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
|  `*`userHandle`*`  | `xsd:string`  | No  | The handle to the company whose group membership you want to remove.  |
|  `*`groupHandleArray`*`  | `types:HandleArray`  | Yes  | The array of handles to groups from which you want the company to be removed.  |

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
