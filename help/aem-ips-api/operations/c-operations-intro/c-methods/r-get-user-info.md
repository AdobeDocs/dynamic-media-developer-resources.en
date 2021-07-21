---
description: Gets information about a user. Use the email address and the password of a system user as credentials for authorizing the request. Otherwise, the operation gets information about the default user.
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
---
# getUserInfo{#getuserinfo}

Gets information about a user. Use the email address and the password of a system user as credentials for authorizing the request. Otherwise, the operation gets information about the default user.

 Syntax 

## Authorized User Types {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-e87b3cb743494719925c9458eed433b6}

**Input (getUserInfoParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`userHandle`*`  | `xsd:string`  | No  | Handle to the user whose information you want to return.  |
|  `*`email`*`  | `xsd:string`  | No  | User email address.  |

**Output (getUserInfoReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`userInfo`*`  | `types:User`  | Yes  | The first name, last name, email address, and role of a user, as well as whether the user is valid and when the user’s password expires.  |

## Examples {#section-98d77a2e360a438dbe240099bea26a65}

This code sample returns information for the default IPS user.

**Request** 

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**Response** 

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```
