---
description: Creates an image format.
seo-description: Creates an image format.
seo-title: saveImageFormat
solution: Experience Manager
title: saveImageFormat
uuid: b11ea668-7a82-439c-b16b-909dc86c00a2
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Administrator"
---

# saveImageFormat{#saveimageformat}

Creates an image format.

>[!NOTE]
>
>The `urlModifier` field value must consist of valid XML. For example, change `&` to `&`. Get the `urlModfier` value from the IPS user interface.

## Authorized User Types {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser` 
* `IpsAdmin` 
* `IpsCompanyAdmin` 
* `ImagePortalAdmin`

## Parameters {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Input (saveImageFormatParam)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`companyHandle`*`  | `xsd:string`  | Yes  | The handle to the company with the image format you want to work with.  |
|  `*`imageFormatHandle`*`  | `xsd:string`  | No  | Image format handle you want to save.  |
|  `*`name`*`  | `xsd:string`  | Yes  | Image format name.  |
|  `*`urlModifier`*`  | `xsd:string`  | Yes  | This can be any IPS protocol query string. The easiest way to generate a URL modifier is to create one with the IPS user interface and then cut and paste the query string.  |

**Output (saveImageFormatReturn)** 

|  Name  | Type  | Required  | Description  |
|---|---|---|---|
|  `*`imageFormatHandle`*`  | `xsd:string`  | Yes  | Handle to the image format.  |

## Examples {#section-c7bd733212ef494297a97093f3af193f}

This code sample creates an image format. In this example, `urlModifier` was determined by its value in the IPS user interface with a valid HTML format.

**Request** 

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**Response** 

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```

