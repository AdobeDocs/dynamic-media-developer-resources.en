---
description: Gets all users in an array.
seo-description: Gets all users in an array.
seo-title: getAllUsers
solution: Experience Manager
title: getAllUsers
uuid: 7fe6ee2a-986d-464d-bc15-1e6444bcf13b
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# getAllUsers{#getallusers}

Gets all users in an array.

 Syntax 

## Authorized User Types {#section-68ed5f5fcc5348308dfe074c590caeaa}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-f092ca72f2024d66a1cec690aeab870a}

**Input (getAllUsersParam)** 

<table id="table_1FE6DDADBD134E6D8BD4B52F1EAD2E85"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Required </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeInvalid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4">Set to: 
    <ul id="ul_FB9F59A8293B4CCA98E42EBF8412C77B"> 
     <li id="li_3C2E6C4D3478411FA1A34D5CBFFC8108"><span class="codeph"> true</span> to include invalid users. </li> 
     <li id="li_7FCA0DE4BE2248A690076FEC6854F5CE"><span class="codeph"> false</span> to omit invalid users. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getAllUsersReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`userArray`*`  | `types:UserArray`  | Yes  | Array of all users.  |
|  `*`Code Phrase`*`  | `Code Phrase`  |  |  |

## Examples {#section-9c9a2d335513478da20652c1b1443731}

This code sample returns all users. The response is truncated for brevity.

**Request** 

```java
<ns1:getAllUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getAllUsersParam>
```

**Response** 

```java
<ns1:getAllUsersReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userArray>
      <ns1:items>
         <ns1:userHandle>201|agentshadi@hotmail.com</ns1:userHandle>
         <ns1:firstName>333</ns1:firstName>
         <ns1:lastName>333</ns1:lastName>
         <ns1:email>my_email@someaddress.com</ns1:email>
         <ns1:role>TrialSiteUser</ns1:role>
         <ns1:isValid>true</ns1:isValid>
         <ns1:passwordExpires>2006-12-29T04:19:43.039Z</ns1:passwordExpires>
      </ns1:items>
   ...
   </ns1:userArray>
<ns1:getAllUsersReturn>
```

