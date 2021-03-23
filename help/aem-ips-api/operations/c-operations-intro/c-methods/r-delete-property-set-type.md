---
description: Deletes a property set type and its associated property set and properties.


solution: Experience Manager
title: deletePropertySetType

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# deletePropertySetType{#deletepropertysettype}

Deletes a property set type and its associated property set and properties.

 Syntax 

## Authorized User Types {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-1c8973f5d35f44b4a6a483a41609e455}

**Input (deletePropertySetTypeParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`typeHandle`*`  | `xsd:string`  | Yes  | The handle to the property set type to be deleted.  |

**Output (deletePropertySetTypeParam)**

The IPS API does not return a response for this operation.

## Examples {#section-85faa2e3411a4e23aa6489037f7ce078}

This code sample uses the type’s handle as a field in the `deletePropertySetTypeParam` sent to the IPS Web services server in order to delete the property set type.

**Request** 

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Response**

None. 
