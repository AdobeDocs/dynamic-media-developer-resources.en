---
description: Gets the users that belong to a specific company and group.
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
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
