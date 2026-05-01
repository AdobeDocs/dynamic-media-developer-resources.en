---
description: Adds new tag values to the dictionary of an existing tag field.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
TQID: https://experienceleague.adobe.com/s--2g8Oye8csgArreYlndh-r-ONCW-lFKp4Oqx4024o
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
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
|  companyHandle  | `xsd:string`  | Yes  | The handle of the company containing the tag field.  |
|  fieldHandle  | `xsd:string`  | Yes  | The handle of the tag field to be modified.  |
|  valueArray  | `xsd:string`  | Yes  | An array of tag values to add to the field's existing dictionary.  |

**Output (addTagFieldValuesParam)**

The IPS API does not return a response for this operation.

## Examples {#section-c4049392f1c548f883b8b1f8f167bada}

**Request** 

```java {.line-numbers}
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
