---
description: A system field search condition for the searchAssets operation.
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
TQID: 'https://experienceleague.adobe.com/dCZl4pLGuG5hHpEq04W-qv8mRWcFiA7PvmzcO7Un-sM'
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
# [!DNL SystemFieldCondition]{#systemfieldcondition}

A system field search condition for the searchAssets operation.

 For unary compares, pass exactly one value ( `boolVal`, `longVal`, `doubleVal`, or `dateVal`) depending on the system field type. For search ranges, pass `min<Type>` and `max<Type>` parameters and pass an `op` value of `Between` or `NotBetween`. 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  field  | `xsd:string`  | Choice of Asset Search System Fields.  |
|  op  | `xsd:string`  | Choice of String Comparison Operators.  |
|  value  | `xsd:string`  | Value to test against.  |
|  boolVal  | `xsd:boolean`  | Boolean comparison value.  |
|  longVal  | `xsd:long`  | Long comparison value.  |
|  minLong  | `xsd:long`  | Lower boundary of long range.  |
|  maxLong  | `xsd:long`  | Upper boundary of long range.  |
|  doubleVal  | `xsd:double`  | Double comparison value.  |
|  minDouble  | `xsd:double`  | Lower boundary of double range.  |
|  maxDouble  | `xsd:double`  | Upper boundary of double range.  |
|  dateVal  | `xsd:dateTime`  | Date comparison value.  |
|  minDate  | `xsd:dateTime`  | Date range minium.  |
|  maxDate  | `xsd:dateTime`  | Date range maximum.  |

## Example {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```

