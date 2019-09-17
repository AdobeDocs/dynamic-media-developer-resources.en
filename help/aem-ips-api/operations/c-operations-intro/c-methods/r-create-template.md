---
description: Creates a layered image that can have multiple text and image layers.
seo-description: Creates a layered image that can have multiple text and image layers.
seo-title: createTemplate
solution: Experience Manager
title: createTemplate
topic: Scene7 Image Production System API
uuid: c54bd47c-13e1-4b0d-a24c-9829b0a6d5bf
---

# createTemplate{#createtemplate}

Creates a layered image that can have multiple text and image layers.

 The `urlModifier` parameter specifies the Image Server protocol commands stored in the Image Server catalog applied prior to any user-supplied commands on the URL. The `urlPostApplyModifier` parameter specifies protocol commands applied after any URL commands, which will override any conflicting user-supplied settings. 

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
|  ` *`companyHandle`*`  | `xsd:string`  | Yes  | The company that the template belongs to.  |
|  ` *`folderHandle`*`  | `xsd:string`  | Yes  | The folder handle that represents the folder where the template resides.  |
|  ` *`name`*`  | `xsd:string`  | Yes  | Template name.  |
|  ` *`type`*`  | `xsd:string`  | Yes  | Template type.  |
|  ` *`urlModifier`*`  | `xsd:string`  | Yes  | Specifies the Image Server commands stored in the IS catalog that are applied prior to any user-supplied commands on the URL.  |
|  ` *`urlPostApplyModifier`*`  | `xsd:string`  | No  | Specifies protocol commands applied after any URL commands, which will override any conflicting user-supplied settings.  |

**Output (createTemplateParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  ` *`assetHandle`*`  | `xsd:string`  | Yes  | The handle to the template.  |

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

