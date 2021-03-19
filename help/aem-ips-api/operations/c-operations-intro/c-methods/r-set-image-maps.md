---
description: Sets the image map for an asset.
seo-description: Sets the image map for an asset.
seo-title: setImageMaps
solution: Experience Manager
title: setImageMaps
uuid: 1dd7e032-34b4-464d-8ec6-7ad282d12891
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Administrator"
---

# setImageMaps{#setimagemaps}

Sets the image map for an asset.

 You must have already created the image maps. Image maps are applied in order of retrieval from the array. This means the second image map overlays the first, the third overlays the second, and so on. 

## Authorized User Types {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-2292ec1aead947ef8741dd0653a41f42}

**Input (setImageMapsParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | Company handle.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | Asset handle.  |
|  `*`imageMapArray`*`  | `types:ImageMapDefinitionArray`  | Yes  | Array of predefined image maps.  |

**Output (setImageMapsReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`imageMapHandleArray`*`  | `types:HandleArray`  | Yes  | An array with image map handles applied to the asset.  |

## Examples {#section-fe2e35662a6a4ee29cf250c9fd180371}

This code sample sets 2 image maps for an image asset. The code specifies shape type, region, and action taken when the image maps are invoked. The response contains an array with handles to the image maps.

**Request** 

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```

