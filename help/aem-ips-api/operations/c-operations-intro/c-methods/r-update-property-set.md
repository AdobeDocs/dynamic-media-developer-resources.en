---
description: Uses a property array to update a property set.


solution: Experience Manager
title: updatePropertySet

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# updatePropertySet{#updatepropertyset}

Uses a property array to update a property set.

 Syntax 

## Authorized User Types {#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-98361b063e9c41e8b2f744fabc0e13ed}

**Input (updatePropertySetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`setHandle`*`  | `xsd:string`  | Yes  | Handle to the property set.  |
|  `*`replaceProperties`*`  | `xsd:string`  | No  |Set to `true` to replace properties.  |
|  `*`propertyArray`*`  | `types:PropertyArray`  | Yes  | Array of updated properties for the property set.  |

**Output (updatePropertySetReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

This code sample updates a property set with properties in the property array.

**Request** 

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**Response**

None. 
