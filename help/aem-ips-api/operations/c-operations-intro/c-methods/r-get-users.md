---
description: Gets an array of users as specified by company, group, and user role handles. This operation lets you sort returned users and filter by character.
seo-description: Gets an array of users as specified by company, group, and user role handles. This operation lets you sort returned users and filter by character.
seo-title: getUsers
solution: Experience Manager
title: getUsers
topic: Scene7 Image Production System API
uuid: f16ccd1b-0f00-4d9a-b6e1-6abc3bde1af9
index: y
internal: n
snippet: y
---

# getUsers{#getusers}

Gets an array of users as specified by company, group, and user role handles. This operation lets you sort returned users and filter by character.

## Authorized User Types {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`


|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`includeInactive`*`  | `xsd:boolean`  | No  | Include or exclude inactive users. Non-IPS Admin users must be an active member of at least one company to be authorized to make any API calls. An authorization fault will be returned if the user has no active company memberships.  |
|  ` *`includeInvalid`*`  | `xsd:boolean`  | No  | Lets you include/exclude invalid users.  |
|  ` *`companyHandleArray`*`  | `types:HandleArray`  | No  | Filter results by company.  |
|  ` *`groupHandleArray`*`  | `types:HandleArray`  | No  | Filter results by group.  |
|  ` *`userRoleArray`*`  | `types:StringArray`  | No  | Filter results by user role.  |
|  ` *`charFilterField`*`  | `xsd:string`  | No  |Filter results by field's string prefix (see [!DNL Trash State).]  |
|  ` *`charFilter`*`  | `xsd:string`  | No  | Filter results by a specific character.  |
|  ` *`sortBy`*`  | `xsd:string`  | No  | Choice of user sort fields.  |
|  ` *`recordsPerPage`*`  | `xsd:int`  | No  | Returns specified number of records per page.  |
|  ` *`resultsPage`*`  | `xsd:int`  | No  | Results page.  |

**Output (getUsersReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`userArray`*`  | `types:UserArray`  | Yes  | An array of users.  |

## Examples {#section-bc43a5dd7b4c4f048d25fc881554dab2}

This code sample returns the array of users for several optional parameters. User roles, user character filter fields, and user sort fields are determined by using specific String Constants.

**Request** 

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**Response** 

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```

