---
description: A system field search condition for the searchAssets operation.
seo-description: A system field search condition for the searchAssets operation.
seo-title: SystemFieldCondition
solution: Experience Manager
title: SystemFieldCondition
topic: Scene7 Image Production System API
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
index: y
internal: n
snippet: y
---

# SystemFieldCondition{#systemfieldcondition}

A system field search condition for the searchAssets operation.

 For unary compares, pass exactly one value ( `boolVal`, `longVal`, `doubleVal`, or `dateVal`) depending on the system field type. For search ranges, pass `min<Type>` and `max<Type>` parameters and pass an `op` value of `Between` or `NotBetween`. 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  ` *`field`*`  | `xsd:string`  | Choice of Asset Search System Fields.  |
|  ` *`op`*`  | `xsd:string`  | Choice of String Comparison Operators.  |
|  ` *`value`*`  | `xsd:string`  | Value to test against.  |
|  ` *`boolVal`*`  | `xsd:boolean`  | Boolean comparison value.  |
|  ` *`longVal`*`  | `xsd:long`  | Long comparison value.  |
|  ` *`minLong`*`  | `xsd:long`  | Lower boundary of long range.  |
|  ` *`maxLong`*`  | `xsd:long`  | Upper boundary of long range.  |
|  ` *`doubleVal`*`  | `xsd:double`  | Double comparison value.  |
|  ` *`minDouble`*`  | `xsd:double`  | Lower boundary of double range.  |
|  ` *`maxDouble`*`  | `xsd:double`  | Upper boundary of double range.  |
|  ` *`dateVal`*`  | `xsd:dateTime`  | Date comparison value.  |
|  ` *`minDate`*`  | `xsd:dateTime`  | Date range minium.  |
|  ` *`maxDate`*`  | `xsd:dateTime`  | Date range maximum.  |

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

