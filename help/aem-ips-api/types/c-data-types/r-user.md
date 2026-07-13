---
description: A user of resources and types in the system.
solution: Experience Manager
title: User
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
TQID: 'https://experienceleague.adobe.com/XM-2FjVie-j71W3Sc3-TypNJUFnz5AQuZZuGOx1fePs'
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
# [!DNL User]{#user}

A user of resources and types in the system.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  userHandle  | `xsd:string`  | User handle.  |
|  firstName  | `xsd:string`  | User first name.  |
|  lastName  | `xsd:string`  | User last name.  |
|  email  | `xsd:string`  | email address.  |
|  defaultRole  | `xsd:string`  |Sets the role for a user in each company they belong to. However, the user role `IpsAmin` overrides other user roles.  |
|  isValid  | `xsd:boolean`  | Determines if the user is valid.  |
|  passwordExpires  | `xsd:dateTime`  | Sets password expiration date.  |

