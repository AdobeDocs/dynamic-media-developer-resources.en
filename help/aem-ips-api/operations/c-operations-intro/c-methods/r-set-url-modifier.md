---
description: Sets the Image Serving or Image Rendering protocol commands for the specified asset. These commands modify the representation of the asset without destroying it.


solution: Experience Manager
title: setUrlModifier

feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
---

# setUrlModifier{#seturlmodifier}

Sets the Image Serving or Image Rendering protocol commands for the specified asset. These commands modify the representation of the asset without destroying it.

 For Image Serving, commands in the `urlModifier` parameter are published in the Modifier catalog field and applied prior to any commands specified on the request URL. Commands in `urlPostApplyModifier` will be published to the `PostModifier` catalog field and will override any commands on the request URL or in `urlModifier`. For Image Rendering, the commands in `urlModifier` and `urlPostApplyModifier` are concatenated and published to the Modifier catalog field. 

## Authorized User Types {#section-fefcd732ccf64c78956606538f96c73d}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-3304fe49bbe24ea1a886e19aaf41fb7d}

**Input (setUrlModifierParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | Company handle.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | Asset handle.  |
|  `*`urlModifier`*`  | `xsd:string`  | No  |Image Serving or Image Rendering protocol commands to apply prior to request or `urlPostApplyModifier` commands.  |
|  `*`urlPostApplyModifier`*`  | `xsd:string`  | No  |Image Serving or Image Rendering protocol commands to apply after `urlModifier` and request commands.  |

**Output (setUrlModifierReturn)**

The IPS API does not return a response for this operation.

## Examples {#section-801d4b9b986443f59a5783a3d6bf44aa}

**Request** 

```java
<setUrlModifierParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|942|1|579</assetHandle>
   <urlModifier>modify=that</urlModifier>
   <urlPostApplyModifier>action=awesomeToo</urlPostApplyModifier>
</setUrlModifierParam>
```

**Response**

None. 
