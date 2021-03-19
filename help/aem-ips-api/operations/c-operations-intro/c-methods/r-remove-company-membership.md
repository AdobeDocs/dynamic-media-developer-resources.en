---
description: Removes a user from one or more companies.
seo-description: Removes a user from one or more companies.
seo-title: removeCompanyMembership
solution: Experience Manager
title: removeCompanyMembership
uuid: af57fde0-2297-41da-87bf-f063fc313264
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# removeCompanyMembership{#removecompanymembership}

Removes a user from one or more companies.

 Syntax 

## Authorized User Types {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Input (removeCompanyMembershipParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`userHandle`*`  | `xsd:string`  | No  | The handle to the user with the membership you want to remove.  |
|  `*`companyHandleArray`*`  | `types:HandleArray`  | Yes  | The handle to the company that you're removing the user from.  |

**Output (removeCompanyMembershipReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-6b7903195e8647a1bd0502f87387ca62}

This code sample removes a user from a company. Omit the optional user handle to remove all users from the companies specified in the company handle array.

**Request** 

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**Response**

None. 
