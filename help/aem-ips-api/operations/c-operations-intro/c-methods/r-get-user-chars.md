---
description: Gets a list of the characters used in a particular field.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
TQID: 'https://experienceleague.adobe.com/ojFrVXletWbKwGTjfJIfRI9M9BBJT7zj4AGrvVMP6T8'
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
# getUserChars{#getuserchars}

Gets a list of the characters used in a particular field.

 Syntax 

## Authorized User Types {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-93107d87f1b24fc8ad276dfee5e30b63}

**Input (getUserCharsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  charField  | `xsd:string`  | Yes  | Determines the Trash State to search for.  |
|  includeInactive  | `xsd:boolean`  | Yes  | Include or exclude inactive users. Non-IPS Admin users must be an active member of at least one company to be authorized to make any API calls. An authorization fault is returned if the user has no active company memberships.  |
|  includInvalid  | `xsd:boolean`  | No  | Include or exclude invalid users.  |
|  companyHandleArray  | `types:HandleArray`  | No  | Filter results based on company.  |
|  groupHandleArray  | `types:HandleArray`  | No  | Filters results based on groups.  |
|  userRoleArray  | `types:StringArray`  | No  | Filters results based on user role.  |
|  numChars  | `xsd:int`  | No  | Enable >1 character.  |

**Output (getUserCharsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  userCharsArray  | `types:StringArray`  | Yes  | An array of character prefixes.  |

## Examples {#section-3702f165e8b041139a6144f4a76ca25f}

This code sample returns:

* First characters of the last names of the users of a specific company. 
* A set of groups. 
* A set of user roles.

The User Char Filter Fields string constant determines the type of user characters returned.

**Request** 

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**Response** 

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```
