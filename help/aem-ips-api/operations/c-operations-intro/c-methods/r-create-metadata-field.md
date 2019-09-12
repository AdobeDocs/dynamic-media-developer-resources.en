---
description: Lets administrators create new metadata fields to coordinate with content management systems or for template operations. Examples of created metadata fields include keywords, information about the author of the image, or copyright holder information.
seo-description: Lets administrators create new metadata fields to coordinate with content management systems or for template operations. Examples of created metadata fields include keywords, information about the author of the image, or copyright holder information.
seo-title: createMetadataField
solution: Experience Manager
title: createMetadataField
topic: Scene7 Image Production System API
uuid: 50ab61fa-df44-4305-ad9f-693c4aea1e69
index: y
internal: n
snippet: y
---

# createMetadataField{#createmetadatafield}

Lets administrators create new metadata fields to coordinate with content management systems or for template operations. Examples of created metadata fields include keywords, information about the author of the image, or copyright holder information.

 Syntax 

## Authorized User Types {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## Parameters {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**Input (createMetadataFieldParam)** 

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Parameter name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Required </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Name of the company the metadata field belongs to. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Asset type. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4"> Name of the metadata field that you are creating. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Yes </td> 
   <td colname="col4">Metadata field type. <p>The metadata field types constant defines the available types. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>The default value of the metadata field to be created (for example, <span class="codeph"> Scene 7</span>). </p> <p>Default values are not supported for tag field types and must be omitted. If a non-empty default is specified for a tag field type, a fault will be returned. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Hide or expose IPS system-specific metadata. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>A boolean flag that indicates whether the metadata field is enforced (validated) when the value is set. </p> <p>If set to true, then a fault is thrown if an illegal value is set in <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Allows you create a set of shared enumerated values that selected tags can point to. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createMetadataFieldReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`fieldHandle`*`  | `xsd:string`  | Yes  | The handle to the new metadata field.  |

## Examples {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

This code sample creates a string type metadata field called `createMetadataField`. The response returns the handle to the new metadata field.

**Request** 

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**Response** 

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```

