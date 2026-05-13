---
description: Gets the users that belong to a specific company and group.
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
TQID: 'https://experienceleague.adobe.com/30uti0zOBWTPoFORCa3fTaGznpYjTcSO7oV7M3E-A1c'
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
# getGroupMembers{#getgroupmembers}

Gets the users that belong to a specific company and group.

 Syntax 

## Authorized User Types {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-b798b06354c946abbb90fa72cc9c67fd}

**Input (getGroupMembersParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company.  |
|  groupHandle  | `xsd:string`  |  | The handle to the group.  |

**Output (getGroupMembersReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  userHandleArray  | `type:HandleArray`  | Yes  | An array of user handles.  |

## Examples {#section-aaa340dba6b64cce9bcd8303cf999166}

This code sample returns a user handle array containing all users that belong to a specific group.

**Request** 

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**Response** 

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```
