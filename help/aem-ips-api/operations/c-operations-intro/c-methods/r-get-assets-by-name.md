---
description: Returns assets based on an array of asset names.
seo-description: Returns assets based on an array of asset names.
seo-title: getAssetsByName
solution: Experience Manager
title: getAssetsByName
topic: Scene7 Image Production System API
uuid: 5b30cd04-9b1d-420c-84b3-2d5a2ccbc776
index: y
internal: n
snippet: y
---

# getAssetsByName{#getassetsbyname}

Returns assets based on an array of asset names.

 Syntax 

## Authorized User Types {#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

>[!NOTE]
>
>Only returns assets to which the user has read access.

## Parameters {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**Input (getAssetsByNameParam)** 

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> The handle to the company. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Provides access as another user. Available to administrators only. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Used to filter by a specific group. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Array of asset names to retrieve. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Array of asset types allowed for retrieved assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Array of Asset Types excluded for retrieved assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Array of asset subtypes allowed for retrieved assets. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>If <span class="codeph"> true</span> and <span class="codeph"> assetSubTypeArray</span> is not empty, only assets whose subtypes are in <span class="codeph"> assetSubTypeArray</span> are returned. </p> <p>If <span class="codeph"> false</span>, then assets with no defined subtype are included. </p> <p>The default value is <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Contains a list of fields and subfields included in the response. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Contains a list of fields and subfields excluded from the response. </td> 
  </tr> 
 </tbody> 
</table>

**Output (getAssetsByNameReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`assetArray`*`  | `types:AssetArray`  | No  | Array of assets that match the filter criteria.  |

## Examples {#section-3b7447398e574c88aeaf8ca159cc78dd}

This code sample returns two image type assets.

**Request** 

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**Response** 

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```

