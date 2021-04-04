---
description: Returns a cropped region for an image based on its background color or transparency.
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: e291597a-b863-42dd-88dc-13398b734410
---
# getAutoCropRect{#getautocroprect}

Returns a cropped region for an image based on its background color or transparency.

 Syntax 

## Authorized User Types {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `IpsUser` 
* `ImagePortalAdmin` 
* `ImagePortalUser` 
* `ImagePortalContrib` 
* `ImagePortalContribUser`

## Parameters {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**Input (getAutoCropRectParam)**

>[!NOTE]
>
>Specify either `*`autoColorCropOptions`*` or `*`autoTransparentCropOptions`*` when calling this method.

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company with the asset you want to work with.  |
|  `*`assetHandle`*`  | `xsd:string`  | Yes  | The handle to the asset you want to work with.  |
|  `*`autoColorCropOptions`*`  | `types:AutoColorCropOptions`  | No  |Compute crop rectangle based on color. See [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6).  |
|  `*`autoTransparentCropOptions`*`  | `types:AutoTransparentCropOptions`  | No  |Compute crop rectangle based on transparency. See [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b).  |

**Output (getAutoCropRectReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`xOffset`*`  | `xsd:int`  | Yes  | The starting left pixels coordinate of the computed crop region.  |
|  `*`yOffset`*`  | `xsd:int`  | Yes  | The starting top pixel coordinate of the computed crop region.  |
|  `*`width`*`  | `xsd:int`  | Yes  | Width of the computed crop region (in pixels).  |
|  `*`height`*`  | `xsd:int`  | Yes  | Height of the computed crop region (in pixels).  |

## Examples {#section-ba65bd66086d491cad1cea535954ee1f}

**Request** 

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**Response** 

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)
