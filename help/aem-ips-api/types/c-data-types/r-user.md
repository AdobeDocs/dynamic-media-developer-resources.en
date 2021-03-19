---
description: A user of resources and types in the system.
seo-description: A user of resources and types in the system.
seo-title: User
solution: Experience Manager
title: User
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# User{#user}

A user of resources and types in the system.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`userHandle`*`  | `xsd:string`  | User handle.  |
|  `*`firstName`*`  | `xsd:string`  | User first name.  |
|  `*`lastName`*`  | `xsd:string`  | User last name.  |
|  `*`email`*`  | `xsd:string`  | email address.  |
|  `*`defaultRole`*`  | `xsd:string`  |Sets the role for a user in each company they belong to. However, the user role `IpsAmin` overrides other user roles.  |
|  `*`isValid`*`  | `xsd:boolean`  | Determines if the user is valid.  |
|  `*`passwordExpires`*`  | `xsd:dateTime`  | Sets password expiration date.  |

