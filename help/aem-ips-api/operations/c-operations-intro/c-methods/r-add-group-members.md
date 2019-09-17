---
description: Adds users from a specific company to a specific group.
seo-description: Adds users from a specific company to a specific group.
seo-title: addGroupMembers
solution: Experience Manager
title: addGroupMembers
topic: Scene7 Image Production System API
uuid: 382d36a8-7c93-48e6-a54b-425c5e6414fe
---

# addGroupMembers{#addgroupmembers}

Adds users from a specific company to a specific group.

 Syntax 

## Authorized User Types {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-b28434dcf2ca4b4ea431136aac33913e}

**Input (addGroupMembersParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company.  |
|  ` *`groupHandle`*`  | `xsd:string`  | Yes  | The group handle.  |
|  ` *`userHandleArray`*`  | `types:HandleArray`  | Yes  | An array of handles to users who you want to add to a group.  |

**Output (addGroupMembersParam)**

The IPS API does not return a response for this operation.

## Examples {#section-8f168b528aef4c4fa8c3d41f7686842f}

This example uses ` *`addGroupMembersParam`*` to add a user to a single company. The IPS API does not return a response for this operation.

**Request**

```java
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Response**

None. 
