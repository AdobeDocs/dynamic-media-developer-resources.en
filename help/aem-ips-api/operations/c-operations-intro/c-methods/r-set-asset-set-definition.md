---
description: Updates the set definition for an existing Asset Set.
seo-description: Updates the set definition for an existing Asset Set.
seo-title: setAssetSetDefinition
solution: Experience Manager
title: setAssetSetDefinition
topic: Dynamic Media Image Production System API
uuid: 2a2dce5d-7a01-49af-ac8b-33ae0b234ecc
---

# setAssetSetDefinition{#setassetsetdefinition}

Updates the set definition for an existing Asset Set.

 Syntax 

## Authorized User Types {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**Input (setAssetDefinitionParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company with the asset set.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | Asset set handle  |
|  `*`setDefinition`*`  | `xsd:string`  | Yes  | Definition string. See below.  |

**Output (setAssetSetDefinitionReturn)**

The IPS API does not return a response for this operation.

## setDefinition Parameter: About {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**setDefinition Functions**

Specify `setDefinition` substitution functions in-line. These are resolved during a catalog lookup or on publication. Substitution strings have the format `${<substitution_func>}`, and include the following: 

>[!NOTE]
>
>Handle literals in the parameter lists must be surrounded by brackets `([])`. The text outside of a substitution string gets copied to the output string during resolution.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Substitution Function </th> 
   <th colname="col2" class="entry"> Returns the Asset's </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Primary file path. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Catalog ID. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([ <span class="varname"> asset_handle </span>],[ <span class="varname"> metadata_field_handle </span>]) </span> </td> 
   <td colname="col2"> Metadata value. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Catalog ID. Applies to image-based assets (Image, Adjusted View, Layer View). <p>For other assets, returns the thumb asset's catalog ID (if any). If no thumb asset is associated with the asset, the function returns an empty string. </p> </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition Examples**

This media set definition string: 

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

Resolves to the following at lookup or publication time: 

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## Examples {#section-739b42eec3074cafae285ec015a2d088}

**Request** 

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**Response**

None. 
