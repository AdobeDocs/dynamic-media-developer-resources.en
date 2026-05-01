---
description: Sets the Image Serving or Image Rendering protocol commands for the specified asset. These commands modify the representation of the asset without destroying it.
solution: Experience Manager
title: setUrlModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9e96ffc8-5a38-46b8-9ba8-956c86b32c7a
TQID: https://experienceleague.adobe.com/RWEIaHyNbujGIavV3DxEulF0erGKk2VSHkRc3vm4-G8
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# setUrlModifier{#seturlmodifier}

Sets the Image Serving or Image Rendering protocol commands for the specified asset. These commands modify the representation of the asset without destroying it.

 For Image Serving, commands in the `urlModifier` parameter are published in the Modifier catalog field and applied prior to any commands specified on the request URL. Commands in `urlPostApplyModifier` are published to the `PostModifier` catalog field and override any commands on the request URL or in `urlModifier`. For Image Rendering, the commands in `urlModifier` and `urlPostApplyModifier` are concatenated and published to the Modifier catalog field. 

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
|  companyHandle  | `xsd:string`  | Yes  | Company handle.  |
|  assetHandle  | `xsd:string`  | Yes  | Asset handle.  |
|  urlModifier  | `xsd:string`  | No  |Image Serving or Image Rendering protocol commands to apply prior to request or `urlPostApplyModifier` commands.  |
|  urlPostApplyModifier  | `xsd:string`  | No  |Image Serving or Image Rendering protocol commands to apply after `urlModifier` and request commands.  |

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
