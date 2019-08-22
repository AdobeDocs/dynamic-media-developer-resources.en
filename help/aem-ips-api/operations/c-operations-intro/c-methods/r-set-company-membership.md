---
description: Sets a user’s membership in one or more companies.
seo-description: Sets a user’s membership in one or more companies.
seo-title: setCompanyMembership
solution: Experience Manager
title: setCompanyMembership
topic: Scene7 Image Production System API
uuid: f0a830e8-0df7-4bd2-a554-796d6fd5fa0e
index: y
internal: n
snippet: y
---

# setCompanyMembership{#setcompanymembership}

Sets a user’s membership in one or more companies.

 Syntax 

## Authorized User Types {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-3930dc6a016140178631083563598104}

**Input (setCompanyMembershipParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`userHandle`*`  | `xsd:sting`  | No  | User handle.  |
|  ` *`membershipArray`*`  | `types:CompanyMembershipUpdateArray`  | Yes  | Array of companies.  |

**Output (setCompanyMembershipParam)**

The IPS API does not return a response for this operation.

## Examples {#section-862c0cc32ce0407ab248028e690a8386}

This code sample adds a user to a company. Specify multiple companies in the company handle array if required.

**Request** 

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**Response**

None. 
