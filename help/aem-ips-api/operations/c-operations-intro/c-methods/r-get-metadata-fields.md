---
description: Gets the user-defined metadata fields associated with an asset.
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
TQID: https://experienceleague.adobe.com/S4MJve6ooTZfcgTLhXKEkN2Ht5zeckmVfBUNqtQ6NbI
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
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
|  companyHandle  | `xsd:string`  | Yes  | The company handle.  |
|  assetType  | `xsd:string`  | Yes  | Asset types from which to obtain metadata.  |

**Output (getMetadataFieldsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  Code Phrase  | `Code Phrase`  |  |  |

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
