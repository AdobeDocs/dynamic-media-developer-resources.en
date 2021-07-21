---
description: Gets unique metadata field values.
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: ac5f5667-6c94-425c-bc01-f9df48d16e00
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
