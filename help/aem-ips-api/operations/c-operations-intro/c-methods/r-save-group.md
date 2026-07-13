---
description: Create or edit a group.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
TQID: 'https://experienceleague.adobe.com/VTDPxH7rjfnALgRNc-Md6NLKZfOrRk6CqQhGi0JNZs4'
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
|  companyHandle  | `xsd:string`  | Yes  | The handle to the company with the group you want to save.  |
|  groupHandle  | `xsd:string`  | No  | The handle to the group.  |
|  name  | `xsd:string`  | Yes  | Group name.  |
|  isSystemDefined  | `xsd:boolean`  | Yes  | `false` is default.  |

**Output (saveGroupReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  groupHandle  | `xsd:string`  | Yes  | Group handle.  |

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

