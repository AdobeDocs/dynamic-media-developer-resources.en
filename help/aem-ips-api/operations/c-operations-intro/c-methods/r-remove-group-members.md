---
description: Removes company users from a specific group.
seo-description: Removes company users from a specific group.
seo-title: removeGroupMembers
solution: Experience Manager
title: removeGroupMembers
topic: Scene7 Image Production System API
uuid: dd0ea335-bbd0-43b1-830b-77f32dc39b12
index: y
internal: n
snippet: y
---

# removeGroupMembers{#removegroupmembers}

Removes company users from a specific group.

 **Differences Between Remove Commands**

* `removeGroupMembers`: Removes multiple users from a group. 
* `removeGroupMembership`: Removes an individual user from an array of groups.

## Authorized User Types {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-b5596614a3be4ce5962455884e4636af}

**Input (removeGroupMembersParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company with the users you want to work with.  |
|  ` *`groupHandle`*`  | `xsd:string`  | Yes  | Group handle.  |
|  ` *`userHandleArray`*`  | `types:HandleArray`  | Yes  | An array of handles for users whose group memberships you want to remove.  |

**Output (removeGroupMembersParam)**

The IPS API does not return a response for this operation.

## Examples {#section-9eedac852cea46ec80de6a6928bf97ac}

This code sample removes a user from the specified company. Remove multiple users from a group with the user handle array.

**Request** 

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**Response**

None. 
