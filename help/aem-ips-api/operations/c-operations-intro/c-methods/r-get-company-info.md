---
description: Returns information about the specified company including the company handle, the company name, the root path, and the expiration date. You must specify either companyHandle or companyName whose information you want to retrieve.
seo-description: Returns information about the specified company including the company handle, the company name, the root path, and the expiration date. You must specify either companyHandle or companyName whose information you want to retrieve.
seo-title: getCompanyInfo
solution: Experience Manager
title: getCompanyInfo
uuid: 9218cba8-2873-46b7-90e3-7ab9d5018690
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Administrator"
---

# getCompanyInfo{#getcompanyinfo}

Returns information about the specified company including the company handle, the company name, the root path, and the expiration date. You must specify either companyHandle or companyName whose information you want to retrieve.

 Syntax 

## Authorized User Types {#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser` 
* `IpsAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-7dec8871c89a414c9f066adade1831d8}

**Input (getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Required </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Either <span class="codeph"> <span class="varname"> companyHandle</span> </span> or <span class="codeph"> <span class="varname"> companyName</span> </span> is required. </p> </td> 
   <td colname="col4"> <p>The handle of the company whose information you want to obtain. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Either <span class="codeph"> <span class="varname"> companyHandle</span> </span> or <span class="codeph"> <span class="varname"> companyName</span> </span> is required. </p> </td> 
   <td colname="col4"> <p>The name of the company whose information you want to obtain. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Required </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:Company</span> </p> </td> 
   <td colname="col3"> <p>Yes </p> </td> 
   <td colname="col4"> <p>Handle and other descriptive information about the company. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Examples {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

This code sample returns all information about a company by using a company name and handle. It returns data similar to the response received when creating a company.

**Request**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**Response**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```

