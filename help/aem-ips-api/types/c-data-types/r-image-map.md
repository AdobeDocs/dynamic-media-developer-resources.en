---
description: Target for a click action in the browser.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
---
# ImageMap{#imagemap}

Target for a click action in the browser.

 Always associated with an image. You can get an `ImageMap` target from `ImageInfo`. 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  imageMapHandle  | `xsd:string`  | Image map handle.  |
|  name  | `xsd:string`  | Image map name.  |
|  region  | `xsd:string`  |Image map coordinates. Format is based on the HTML `<area>` tag attribute.  |
|  action  | `xsd:string`  |Other attributes to include in the HTML `<area>` tag, including the `href` URL.  |
|  shapeType  | `xsd:boolean`  |A [!DNL RegionShape] value.  |
|  position  | `xsd:string`  |Position in the format of the HTML `<area>` element’s [!DNL coords] attribute. For example: `coords ="0,0,84,128"`.  |
|  enabled  | `xsd:boolean`  | True if image map is enabled.  |
|  lastModified  | `xsd:dateTime`  | Date and time the image map was last modified.  |
