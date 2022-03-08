---
description: Sets tag dictionary values for an existing tag field.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
---
# setTagFieldValues{#settagfieldvalues}

Sets tag dictionary values for an existing tag field.

 Syntax 

## Authorized User Types {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-a05cbee4cb4f44198c414a6b14e69156}

**Input** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | Company handle.  |
|  fieldHandle  | `xsd:string`  | Yes  | Tag field handle.  |
|  valueArray  | `types:StringArray`  | Yes  | An array of tag values that replace the field's existing dictionary. Asset associations are maintained when a new value matches an existing value.  |

**Output (setTagFieldValuesReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-b11cafd9bed54ab5836c737cc075c918}

**Request** 

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**Response**

None.
