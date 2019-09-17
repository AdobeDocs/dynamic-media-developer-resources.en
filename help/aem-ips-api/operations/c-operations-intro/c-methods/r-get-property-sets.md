---
description: Gets property sets associated with a type handle.
seo-description: Gets property sets associated with a type handle.
seo-title: getPropertySets
solution: Experience Manager
title: getPropertySets
topic: Scene7 Image Production System API
uuid: fa3cadb3-92b3-4ffb-ac1e-87a01b98bcb2
---

# getPropertySets{#getpropertysets}

Gets property sets associated with a type handle.

 Syntax 

## Authorized User Types {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `TrialSiteUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-d8da2847e77e4a95a4441d9848cac775}

**Input (getPropertySetsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`typeHandle`*`  | `xsd:string`  | Yes  | The handle to the property set type.  |
|  ` *`primaryOwnerHandle`*`  | `xsd:string`  | Yes  | The primary owner of the data bound to the database object.  |
|  ` *`secondaryOwnerHandle`*`  | `xsd:string`  | No  | An optional secondary owner of the data.  |

**Output (getPropertySetsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`setArray`*`  | `types:PropertySetArray`  | Yes  | Arry of property sets.  |

## Examples {#section-1358af974eab4259864910337a6f0bd2}

This code sample returns property sets of their primary owner, specified by a type handle.

**Request** 

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**Response** 

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```

