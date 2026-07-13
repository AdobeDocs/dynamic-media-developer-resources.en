---
description: Removes a user from one or more companies.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
TQID: 'https://experienceleague.adobe.com/5jjL8MnUtL046oSej3HErZB9hrD-ueEBC5-h9vD92HM'
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
|  userHandle  | `xsd:string`  | No  | The handle to the user with the membership you want to remove.  |
|  companyHandleArray  | `types:HandleArray`  | Yes  | The handle to the company that you're removing the user from.  |

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

