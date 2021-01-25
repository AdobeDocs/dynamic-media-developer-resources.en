---
description: Gets unique metadata field values.
seo-description: Gets unique metadata field values.
seo-title: getUniqueMetadataValues
solution: Experience Manager
title: getUniqueMetadataValues
topic: Dynamic Media Image Production System API
uuid: 5b2f95a7-cc0b-4938-99b9-2aefa0ffe693
---

# getUniqueMetadataValues{#getuniquemetadatavalues}

Gets unique metadata field values.

 Syntax 

## Authorized User Types {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-b9d1413811c24566b6d095701f0f66db}

**Input (getUniqueMetadataValuesParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | Handle to the company.  |
|  `*`fieldHandle`*`  | `xsd:string`  | No  | Handle to metadata field.  |

**Output (getUniqueMetadataValuesReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`values`*`  | `type:StringArray`  |  |  |

## Examples {#section-440f3bc3e5be436cb6ec26117d05f476}

This code sample uses a field handle to return specific metadata values.

**Request** 

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**Response** 

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```

