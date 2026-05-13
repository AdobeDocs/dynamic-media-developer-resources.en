---
description: Uses a property array to update a property set.
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
TQID: 'https://experienceleague.adobe.com/-z-ZUe9SO-HG05Gv6XQAlREi2wrP93lH-HFEwNOxENI'
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
|  setHandle  | `xsd:string`  | Yes  | Handle to the property set.  |
|  replaceProperties  | `xsd:string`  | No  |Set to `true` to replace properties.  |
|  propertyArray  | `types:PropertyArray`  | Yes  | Array of updated properties for the property set.  |

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
