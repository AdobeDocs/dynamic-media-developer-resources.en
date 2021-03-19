---
description: Checks if a user with a specific company (identified by handle), email address, and password can log in.
seo-description: Checks if a user with a specific company (identified by handle), email address, and password can log in.
seo-title: checkLogin
solution: Experience Manager
title: checkLogin
uuid: 69f9e5f6-50c2-403d-93b2-b84a01f512a9
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# checkLogin{#checklogin}

Checks if a user with a specific company (identified by handle), email address, and password can log in.

>[!NOTE]
>
>If the company handle is omitted, this method checks the login of the default user.

## Authorized User Types {#section-df8b26b550854f899948276adaca083a}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-1ad4c0b4803b4388aedd655030676cb3}

**Input (checkLoginParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | No  | The handle to the company that contains the user.  |
|  `*`email`*`  | `xsd:string`  | Yes  | The user's email address.  |
|  `*`password`*`  | `xsd:string`  | Yes  | The user's password.  |

**Output (checkLoginParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`status`*`  | `xsd:string`  | Yes  | User's log in status.  |

## Examples {#section-23f90100a9d94bc7b4045634cccd1b98}

This sample code uses a company handle parameter, email address, and a password to determine if a user can log in to IPS. If the user *can* log in, this method returns the string, `ValidLogin`. If the user *cannot* log in, this method returns the string, `InvalidLogin`.

**Request** 

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**Response** 

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```

