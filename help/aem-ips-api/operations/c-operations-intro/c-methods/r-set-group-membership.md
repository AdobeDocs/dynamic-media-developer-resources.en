---
description: Sets group membership for a user.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
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
|  `*`userHandle`*`  | `xsd:string`  | No  | The handle to the user whose group membership you want to set.  |
|  `*`companyHandle`*`  | `xsd:string`  | No  | Company handle.  |
|  `*`groupHandleArray`*`  | `types:HandleArray`  | Yes  | The array of handles to groups to which the user to belongs.  |

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
