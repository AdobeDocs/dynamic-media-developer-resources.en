---
description: Property sets are application-specific sets of name-value pairs that can be attached to various IPS objects, depending on the property set type. If the property set type does not allow multiple sets to be attached to an object (PropertySetType/allowMultipleisfalse) and the object already has an associated set of the same type, the new set will replace the existing one.
solution: Experience Manager
title: createPropertySet

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# createPropertySet{#createpropertyset}

Property sets are application-specific sets of name-value pairs that can be attached to various IPS objects, depending on the property set type. If the property set type does not allow multiple sets to be attached to an object (PropertySetType/allowMultipleisfalse) and the object already has an associated set of the same type, the new set will replace the existing one.

 Syntax 

## Authorized User Types {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `TrialSiteAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-25258e75f5f3419bad165c797eb6cd8e}

**Input (createPropertySetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`typeHandle`*`  | `xsd:string`  | Yes  | The handle to the property set type.  |
|  `*`primaryOwnerHandle`*`  | `xsd:string`  | Yes  | The handle to the primary owner of the property set.  |
|  `*`secondaryOwnerHandle`*`  | `xsd:string`  | No  | The handle to the secondary owner of the property set.  |
|  `*`propertyArray`*`  | `types:PropertyArray`  | Yes  | The array of properties.  |
|  `*`permissionArray`*`  | `types:PermissionUpdateArray`  |  |  |

**Output (createPropertySetParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`setHandle`*`  | `xsd:string`  | Yes  | The handle to the new property set.  |

## Examples {#section-4e1f5b2883664bc88f590fcd253df22b}

This code sample creates a property set that contains names and values of properties. The response returns a handle to the new property set.

**Request** 

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**Response** 

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```

