---
description: Target for a click action in the browser.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
TQID: 'https://experienceleague.adobe.com/ikMxCQ23L0HzbfmRlcYGL-fRJFK2uhwbZHNzcy1c25k'
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
# [!DNL ImageMap]{#imagemap}

Target for a click action in the browser.

 Always associated with an image. You can get an `ImageMap` target from `ImageInfo`. 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  imageMapHandle  | `xsd:string`  | Image map handle.  |
|  [!DNL name]  | `xsd:string`  | Image map name.  |
|  [!DNL region]  | `xsd:string`  |Image map coordinates. Format is based on the HTML `<area>` tag attribute.  |
|  [!DNL action]  | `xsd:string`  |Other attributes to include in the HTML `<area>` tag, including the `href` URL.  |
|  shapeType  | `xsd:boolean`  |A [!DNL RegionShape] value.  |
|  [!DNL position]  | `xsd:string`  |Position in the format of the HTML `<area>` element’s [!DNL coords] attribute. For example: `coords ="0,0,84,128"`.  |
|  [!DNL enabled]  | `xsd:boolean`  | True if image map is enabled.  |
|  lastModified  | `xsd:dateTime`  | Date and time the image map was last modified.  |

