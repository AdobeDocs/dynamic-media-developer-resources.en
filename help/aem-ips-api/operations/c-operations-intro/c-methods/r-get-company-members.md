---
description: Returns the users of a company specified by a company handle.
solution: Experience Manager
title: getCompanyMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
TQID: 'https://experienceleague.adobe.com/QMJGqj7IEplTMdFFwVP3UReZAJsi25tHaaMewM30MSU'
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
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# getCompanyMembers{#getcompanymembers}

Returns the users of a company specified by a company handle.

 Syntax 

## Authorized User Types {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-5602e4d6f2214e398e6a804e61f1a088}

**Input (getCompanyMembersParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company whose members you want to obtain.  |
|  includeInvalid  | `xsd:boolean`  | Yes  | Include invalid companies.  |

**Output (getCompanyMembersReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  memberArray  | `types:CompanyMemberArray`  | Yes  | Array of user memberships.  |

## Examples {#section-39d8cf3653fd4fe8b842caabac9dedfc}

This code sample returns all the members of a company in a user array. The response has been truncated for brevity.

**Request** 

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**Response** 

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```
