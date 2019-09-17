---
description: Gets a list of the characters used in a particular field.
seo-description: Gets a list of the characters used in a particular field.
seo-title: getUserChars
solution: Experience Manager
title: getUserChars
topic: Scene7 Image Production System API
uuid: c9fa7826-5174-4298-99e6-a0627e432567
---

# getUserChars{#getuserchars}

Gets a list of the characters used in a particular field.

 Syntax 

## Authorized User Types {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-93107d87f1b24fc8ad276dfee5e30b63}

**Input (getUserCharsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`charField`*`  | `xsd:string`  | Yes  | Determines the Trash State to search for.  |
|  ` *`includeInactive`*`  | `xsd:boolean`  | Yes  | Include or exclude inactive users. Non-IPS Admin users must be an active member of at least one company to be authorized to make any API calls. An authorization fault will be returned if the user has no active company memberships.  |
|  ` *`includInvalid`*`  | `xsd:boolean`  | No  | Include or exclude invalid users.  |
|  ` *`companyHandleArray`*`  | `types:HandleArray`  | No  | Filter results based on company.  |
|  ` *`groupHandleArray`*`  | `types:HandleArray`  | No  | Filters results based on groups.  |
|  ` *`userRoleArray`*`  | `types:StringArray`  | No  | Filters results based on user role.  |
|  ` *`numChars`*`  | `xsd:int`  | No  | Enable >1 character.  |

**Output (getUserCharsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`userCharsArray`*`  | `types:StringArray`  | Yes  | An array of character prefixes.  |

## Examples {#section-3702f165e8b041139a6144f4a76ca25f}

This code sample returns:

* First characters of the last names of the users of a specific company. 
* A set of groups. 
* A set of user roles.

The User Char Filter Fields string constant determines the type of user characters returned.

**Request** 

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**Response** 

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```

