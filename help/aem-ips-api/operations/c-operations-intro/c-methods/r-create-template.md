---
description: Creates a layered image that can have multiple text and image layers.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
TQID: 'https://experienceleague.adobe.com/T9x2yuGOkwJ5xp6CVyREMySIy7HYL58jYI3-J2E2K6g'
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
# createTemplate{#createtemplate}

Creates a layered image that can have multiple text and image layers.

 The `urlModifier` parameter specifies the Image Server protocol commands stored in the Image Server catalog applied prior to any user-supplied commands on the URL. The `urlPostApplyModifier` parameter specifies protocol commands applied after any URL commands, which overrides any conflicting user-supplied settings. 

## Authorized User Types {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser` 
* `IpsAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Input (createTemplateParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  companyHandle  | `xsd:string`  | Yes  | The company that the template belongs to.  |
|  folderHandle  | `xsd:string`  | Yes  | The folder handle that represents the folder where the template resides.  |
|  name  | `xsd:string`  | Yes  | Template name.  |
|  type  | `xsd:string`  | Yes  | Template type.  |
|  urlModifier  | `xsd:string`  | Yes  | Specifies the Image Server commands stored in the IS catalog that are applied prior to any user-supplied commands on the URL.  |
|  urlPostApplyModifier  | `xsd:string`  | No  | Specifies protocol commands applied after any URL commands, which overrides any conflicting user-supplied settings.  |

**Output (createTemplateParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  assetHandle  | `xsd:string`  | Yes  | The handle to the template.  |

## Examples {#section-09adb4d2f0c944af875c4463a461f55d}

This code sample creates a template in a folder specified by a handle, with a name of `APIcreateTemplate`, a `urlModifier`, and a `urlPostApplyModifier`. The response returns the handle to the newly created template.

**Request** 

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**Response** 

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```
