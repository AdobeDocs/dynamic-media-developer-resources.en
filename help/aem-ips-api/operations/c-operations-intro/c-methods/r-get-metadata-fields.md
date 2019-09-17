---
description: Gets the user-defined metadata fields associated with an asset.
seo-description: Gets the user-defined metadata fields associated with an asset.
seo-title: getMetadataFields
solution: Experience Manager
title: getMetadataFields
topic: Scene7 Image Production System API
uuid: bf891bae-53c8-4e3d-90df-caca9a7e022b
---

# getMetadataFields{#getmetadatafields}

Gets the user-defined metadata fields associated with an asset.

 Syntax 

## Authorized User Types {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-bac949e59c0546429c5786fe422d750d}

**Input (getMetadataFieldsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The company handle.  |
|  ` *`assetType`*`  | `xsd:string`  | Yes  | Asset types from which to obtain metadata.  |

**Output (getMetadataFieldsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`Code Phrase`*`  | `Code Phrase`  |  |  |

## Examples {#section-dbfde1483d614b5aac2b491cb32115d7}

This code sample returns metadata assets for the specified type and company. The response contains an array of metadata fields in a field array. Not all assets have the same metadata. The IPS user defines the asset's metadata field.

**Request** 

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**Response** 

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```

