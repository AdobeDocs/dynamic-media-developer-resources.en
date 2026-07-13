---
description: A property set type specifies various settings used to help manage property sets.
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
TQID: 'https://experienceleague.adobe.com/JOAxK9j-P0v8inQRU65C2rVCM9-OnXTXCF6wtp6eksY'
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
# createPropertySetType{#createpropertysettype}

A property set type specifies various settings used to help manage property sets.

 Syntax 

## Authorized User Types {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-43dece72eb9f44df80f4a119dd2c008b}

**Input (createPropertySetTypeParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | No  |The handle to the company that owns the property set type. If `companyHandle` is not passed and the caller is an `IpsAdmin`, a global property set type is created.  |
|  name  | `xsd:string`  | Yes  | The name of the property set type.  |
|  propertyType  | `xsd:string`  | Yes  | Choice of property set types.  |
|  allowMultiple  | `xsd:boolean`  | Yes  | Determines if your program can have multiple property sets.  |

**Output (createPropertySetTypeReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  typeHandle  | `xsd:string`  | Yes  | A handle to the type.  |

## Examples {#section-13396c9639a6475190e622eae3cdb534}

This code sample creates a property set with a name and type specified by the `PropertySet Types` constant. The handle to the company that owns the property set type. If companyHandle is not passed and the caller is an IpsAdmin, a global property set type is created.

**Request** 

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**Response** 

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>

```

