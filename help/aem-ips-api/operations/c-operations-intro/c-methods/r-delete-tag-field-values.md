---
description: Removes tag field values from the dictionary of a tag field.
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
TQID: 'https://experienceleague.adobe.com/SRTriQHWMLXJtkGeS-sCDZE3-1bu1TKNkKjxgESYOi4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# deleteTagFieldValues{#deletetagfieldvalues}

Removes tag field values from the dictionary of a tag field.

## Authorized User Types {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-5db64a6ae238426395bc760b83587260}

**Input (deleteTagFieldValuesParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The handle of the company containing the tag field.  |
|  fieldHandle  | `xsd:string`  | Yes  | The handle of the tag field to be modified.  |
|  valueArray  | `types:StringArray`  | Yes  | An array of tag values to be deleted from the field’s dictionary.  |

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
