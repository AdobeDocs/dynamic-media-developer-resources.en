---
description: Creates a user account and adds that account to one or more companies.
seo-description: Creates a user account and adds that account to one or more companies.
seo-title: addUser
solution: Experience Manager
title: addUser
topic: Scene7 Image Production System API
uuid: aadea419-e65c-471e-ae40-e7de2c1fbb1f
index: y
internal: n
snippet: y
---

# addUser{#adduser}

Creates a user account and adds that account to one or more companies.

 When adding a user to multiple companies, specify those companies by their company handles in `companyHandleArray`. This operation returns the handle to user you just added. 

## Authorized User Types {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-40390a512e314b8d80ecffbb7729f6fb}

**Input (addUserParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`firstName`*`  | `xsd:string`  | Yes  | The user's first name.  |
|  ` *`lastName`*`  | `xsd:string`  | Yes  | The user's last name.  |
|  ` *`email`*`  | `xsd:string`  | Yes  | The user's email address.  |
|  ` *`defaultRole`*`  | `xsd:string`  | Yes  |Sets the role for a user in each company they belong to. Note, however, the `IpsAdmin` role overrides other per-company settings.  |
|  ` *`password`*`  | `xsd:string`  | Yes  | Sets the user's password  |
|  ` *`passwordExpires`*`  | `xsd:dateTime`  | No  | Sets the password expiration period. Provide the time zone when passing in the request. Time zones are adjusted to Central Time.  |
|  ` *`isValid`*`  | `xsd:boolean`  | Yes  | Determines if the user is valid.  |
|  ` *`membershipArray`*`  | `xsd:CompanyMembershipUpdateArray`  | Yes  | An array of company handles.  |

**Output (addUserParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`userHandle`*`  | `xsd:string`  | Yes  | The handle to the user.  |

## Examples {#section-2547cef622734b71919eef849960b5cb}

The IPS API returns a user handle element that specifies the new user.

**Request**

```java
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**Response** 

```java
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```

