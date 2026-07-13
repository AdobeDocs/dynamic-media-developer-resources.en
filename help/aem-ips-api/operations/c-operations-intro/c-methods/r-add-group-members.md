---
description: Adds users from a specific company to a specific group.
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
TQID: 'https://experienceleague.adobe.com/iwy99zQOP-peI6mJgDE8bp7NGN6bjH1g5MBN53gIkJw'
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
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company.  |
|  groupHandle  | `xsd:string`  | Yes  | The group handle.  |
|  userHandleArray  | `types:HandleArray`  | Yes  | An array of handles to users who you want to add to a group.  |

**Output (addGroupMembersParam)**

The IPS API does not return a response for this operation.

## Examples {#section-8f168b528aef4c4fa8c3d41f7686842f}

This example uses addGroupMembersParam to add a user to a single company. The IPS API does not return a response for this operation.

**Request**

```java {.line-numbers}
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Response**

None.

