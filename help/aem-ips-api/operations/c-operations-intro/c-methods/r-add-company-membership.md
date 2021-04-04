---
description: Adds a user to one or more companies.
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
---
# addCompanyMembership{#addcompanymembership}

Adds a user to one or more companies.

 Syntax 

## Authorized User Types {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Input (addCompanyMembershipParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`userHandle`*`  | `xsd:string`  | No  | The handle to the user whose membership you want to add.  |
|  `*`membershipArray`*`  | `types:CompanyMembershipUpdateArray`  | Yes  | An array of companies that you're adding the user to.  |

**Output (addCompanyMembershipReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-5469f88bac7047cca131faa6b021e437}

This example uses `*`companyHandleArray`*` to add a user to a single company.

**Request**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**Response**

None.
