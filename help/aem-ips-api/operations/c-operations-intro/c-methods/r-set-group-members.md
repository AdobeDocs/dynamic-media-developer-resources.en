---
description: Sets the group membership of users that belong to a specific company.


solution: Experience Manager
title: setGroupMembers

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
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
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | Company handle.  |
|  `*`groupHandle`*`  | `xsd:string`  | Yes  | Group handle.  |
|  `*`userHandleArray`*`  | `types:HandleArray`  | Yes  | Array of handles for users whose group membership you want to set.  |

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
