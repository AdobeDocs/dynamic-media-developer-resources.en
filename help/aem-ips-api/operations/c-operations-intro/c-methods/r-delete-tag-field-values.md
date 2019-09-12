---
description: Removes tag field values from the dictionary of a tag field.
seo-description: Removes tag field values from the dictionary of a tag field.
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
topic: Scene7 Image Production System API
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
index: y
internal: n
snippet: y
---

# deleteTagFieldValues{#deletetagfieldvalues}

Removes tag field values from the dictionary of a tag field.

 Syntax 

## Authorized User Types {#section-e6f97c875c2a4cf0a7bc22096b649497}

****

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-5db64a6ae238426395bc760b83587260}

**Input (deleteTagFieldValuesParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle of the company containing the tag field.  |
|  ` *`fieldHandle`*`  | `xsd:string`  | Yes  | The handle of the tag field to be modified.  |
|  ` *`valueArray`*`  | `types:StringArray`  | Yes  | An array of tag values to be deleted from the field’s dictionary.  |

**Output (deleteTagFieldValuesParam)**

The IPS API does not return a response for this operation.

## Examples {#section-92f9e575a6da491caa09e264b4d6ee55}

**Request** 

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**Response**

None. 
