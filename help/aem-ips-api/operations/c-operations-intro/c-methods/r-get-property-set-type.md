---
description: Gets a property set type using a handle to a company and the name of the property set type. It gets a type structure with the handle to the type as well as the property type.
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# getPropertySetType{#getpropertysettype}

Gets a property set type using a handle to a company and the name of the property set type. It gets a type structure with the handle to the type as well as the property type.

 Syntax 

## Authorized User Types {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-c9a53400c44744668bd7915f72d2bf3d}

**Input (getPropertySetTypeParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | No  | The handle to the company. Optional because a property set type can belong to multiple companies.  |
|  `*`name`*`  | `xsd:string`  | Yes  | Property set type name.  |

**Output (getPropertySetTypeReturn)** 

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PropertySetType</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4">The type structure that contains a: 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">Handle. </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">Type name. </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">Property type. </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">Value that indicates if the type allows multiple property types. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Examples {#section-1b57199415e34a8fa449f864f8895b14}

This code sample returns a property set type by name.

**Request** 

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**Response** 

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```

