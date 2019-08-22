---
description: Adds new tag values to the dictionary of an existing tag field.
seo-description: Adds new tag values to the dictionary of an existing tag field.
seo-title: addTagFieldValues
solution: Experience Manager
title: addTagFieldValues
topic: Scene7 Image Production System API
uuid: e114378e-961e-4bf8-8b8b-0071c7a87f37
index: y
internal: n
snippet: y
---

# addTagFieldValues{#addtagfieldvalues}

Adds new tag values to the dictionary of an existing tag field.

 Syntax 

## Authorized User Types {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Input (addTagFieldValuesParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle of the company containing the tag field.  |
|  ` *`fieldHandle`*`  | `xsd:string`  | Yes  | The handle of the tag field to be modified.  |
|  ` *`valueArray`*`  | `xsd:string`  | Yes  | An array of tag values to add to the field's existing dictionary.  |

**Output (addTagFieldValuesParam)**

The IPS API does not return a response for this operation.

## Examples {#section-c4049392f1c548f883b8b1f8f167bada}

**Request** 

```java
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**Response**

None. 
