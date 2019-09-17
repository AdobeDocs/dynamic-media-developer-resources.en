---
description: User-defined field definitions for specific assets.
seo-description: User-defined field definitions for specific assets.
seo-title: MetadataField
solution: Experience Manager
title: MetadataField
topic: Scene7 Image Production System API
uuid: 6156be6e-efa5-4e90-928d-2ab936668154
---

# MetadataField{#metadatafield}

User-defined field definitions for specific assets.

 Retrieve tag field definitions with the `getMetadataFields` or `getAssetMetadataField` operations. 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Metadata field handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Metadata field name. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Metadata field type. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Default value for the metadata field. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isRequired</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Sets required status. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isUserDefined</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Determines if the metadata field is defined by the user or not. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Hide or expose IPS system-specific metadata. Returned from <a href="../../operations/c-operations-intro/c-methods/r-get-metadata-fields.md#reference-170337127801401d9ea54bd4ccf28efe" format="dita" scope="local"> getMetadataFields</a> and <a href="../../operations/c-operations-intro/c-methods/r-get-asset-metadata-fields.md#reference-ea57f8e98d3e443da66114550b0d0a28" format="dita" scope="local"> getAssetMetadataFields</a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>A boolean flag that indicates whether the metadata field type is enforced (validated) when the value is set. </p> <p>If set to true, then a fault is thrown if an illegal value is set in <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Allows you create a set of shared enumerated values that selected tags can point to. </td> 
  </tr> 
 </tbody> 
</table>

