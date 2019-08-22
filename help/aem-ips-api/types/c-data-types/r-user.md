---
description: A user of resources and types in the system.
seo-description: A user of resources and types in the system.
seo-title: User
solution: Experience Manager
title: User
topic: Scene7 Image Production System API
uuid: bdeb8908-7556-44ef-b2f2-12a519903f57
index: y
internal: n
snippet: y
---

# User{#user}

A user of resources and types in the system.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  ` *`userHandle`*`  | `xsd:string`  | User handle.  |
|  ` *`firstName`*`  | `xsd:string`  | User first name.  |
|  ` *`lastName`*`  | `xsd:string`  | User last name.  |
|  ` *`email`*`  | `xsd:string`  | email address.  |
|  ` *`defaultRole`*`  | `xsd:string`  |Sets the role for a user in each company they belong to. However, the user role `IpsAmin` overrides other user roles.  |
|  ` *`isValid`*`  | `xsd:boolean`  | Determines if the user is valid.  |
|  ` *`passwordExpires`*`  | `xsd:dateTime`  | Sets password expiration date.  |

