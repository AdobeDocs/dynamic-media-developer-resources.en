---
description: Creates a generic asset set with a raw set definition string to be published to an Image Server.
seo-description: Creates a generic asset set with a raw set definition string to be published to an Image Server.
seo-title: createAssetSet
solution: Experience Manager
title: createAssetSet
topic: Scene7 Image Production System API
uuid: 1e86bd37-511c-4c12-abfd-075053b86f78
---

# createAssetSet{#createassetset}

Creates a generic asset set with a raw set definition string to be published to an Image Server.

 Syntax 

## Authorized User Types {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-3580b586296e42a5b21426085b1bb72d}

**Input (createAssetSet)** 

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> The handle to the company that will contain the asset set. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> The handle to the folder in which the new asset set will be created. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Asset name. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> A unique identifier created by the client for the asset set type. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> The parameters in the set definition string. <p>These must resolve to the format specified by the target viewer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Handle of the asset that acts as the thumbnail for the new image set. If not specified, IPS tries to use the first image asset referenced by the set. </td> 
  </tr> 
 </tbody> 
</table>

**Substitution Functions for setDefinition**

You can specify substitution functions in line which are resolved during catalog lookup or publication. Substitution strings have the format `${<substitution_func>}`. Available functions are enumerated below. 

>[!NOTE]
>
>The handle literals in parameter lists must be surrounded by brackets `([])`. All text that is outside of a substitution string is copied verbatim to the output string during resolution.

|  **Substitution Function** | **Returns** |
|---|---|
|  `getFilePath([asset_handle>])`  | The asset's master file path.  |
|  `getCatalogId([<asset_handle>])`  | The asset's catalog ID.  |
|  `getMetaData([<asset_handle>], [<metadata_field_handle>])`  | Metadata values for the asset.  |
|  `getThumbCatalogId([<asset_handle>])`  | The asset's catalog ID (for image-based assets only).The associated thumb asset's catalog ID (for other assets). If an associated thumb asset is not available, the function returns an empty string.  |

**Sample Media setDefinition String** 

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 

```

At catalog lookup or publish time, this is resolved to a string similar to the following: 

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Output (createAssetSet)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`assetHandle`*`  | `xsd:string`  | Yes  | The handle to the asset set.  |

## Examples {#section-fed53089de824d67ab96cd9103d384b4}

**Request** 

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**Response** 

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```

