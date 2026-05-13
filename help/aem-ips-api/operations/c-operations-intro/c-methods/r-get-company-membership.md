---
description: Gets a user’s memberships in a company array.
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
TQID: 'https://experienceleague.adobe.com/h-fjzt4o5zdyVkWh9pkWDLs6KXTF3--s4koIQv77Zno'
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
# getCompanyMembership{#getcompanymembership}

Gets a user’s memberships in a company array.

 Syntax 

## Authorized User Types {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-8745c360c3e1400a88e9bdb26bcb93de}

**Input (getCompanyMembershipParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  userHandle  | `xsd:string`  | No  | The handle to the user whose memberships you want to obtain.  |

**Output (getCompanyMembershipReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  membershipArray  | `types:CompanyMembershipArray`  | Yes  | Array of company memberships.  |

## Examples {#section-e4958d104ea344a4a79f57d07b46eba7}

This code sample takes a user handle and gets all the user’s company memberships in an array. The response has been truncated for brevity.

**Request** 

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**Response** 

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```
