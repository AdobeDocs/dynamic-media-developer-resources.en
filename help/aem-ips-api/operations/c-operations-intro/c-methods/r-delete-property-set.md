---
description: Deletes a property set and all associated properties.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
---
# deletePropertySet{#deletepropertyset}

Deletes a property set and all associated properties.

 Syntax 

## Authorized User Types {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-e5fc868f69494cf6858e03027db09101}

**Input (deletePropertySetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  setHandle  | `xsd:string`  | Yes  | The handle to the property set to be deleted.  |

**Output (deletePropertySetParam)**

The IPS API does not return a response for this operation.

## Examples {#section-cf319fc8f86a40ab9cbd838b031973fe}

This code sample uses the set’s handle as a field in the `deletePropertySetParam` sent to the IPS Web services server in order to delete the property set.

**Request** 

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Response**

None.
