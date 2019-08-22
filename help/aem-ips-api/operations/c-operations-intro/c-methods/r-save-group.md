---
description: Create or edit a group.
seo-description: Create or edit a group.
seo-title: saveGroup
solution: Experience Manager
title: saveGroup
topic: Scene7 Image Production System API
uuid: 5efeed17-b07e-41a5-981a-88b754f2629a
index: y
internal: n
snippet: y
---

# saveGroup{#savegroup}

Create or edit a group.

 Syntax 

## Authorized User Types {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-743610e98dd5494baffcbad6401038eb}

**Input (saveGroupParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company with the group you want to save.  |
|  ` *`groupHandle`*`  | `xsd:string`  | No  | The handle to the group.  |
|  ` *`name`*`  | `xsd:string`  | Yes  | Group name.  |
|  ` *`isSystemDefined`*`  | `xsd:boolean`  | Yes  | `false` is default.  |

**Output (saveGroupReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`groupHandle`*`  | `xsd:string`  | Yes  | Group handle.  |

## Examples {#section-26eee227ff1f4edabb7fa1240b4d9999}

This code sample creates a group that belongs to a specific company. If the group already exists, it is saved with the parameter values that you specify.

**Request** 

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**Response** 

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```

