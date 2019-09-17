---
description: Target for a click action in the browser.
seo-description: Target for a click action in the browser.
seo-title: ImageMap
solution: Experience Manager
title: ImageMap
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
---

# ImageMap{#imagemap}

Target for a click action in the browser.

 Always associated with an image. You can get an `ImageMap` target from `ImageInfo`. 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  ` *`imageMapHandle`*`  | `xsd:string`  | Image map handle.  |
|  ` *`name`*`  | `xsd:string`  | Image map name.  |
|  ` *`region`*`  | `xsd:string`  |Image map coordinates. Format is based on the HTML `<area>` tag attribute.  |
|  ` *`action`*`  | `xsd:string`  |Other attributes to include in the HTML `<area>` tag, including the `href` URL.  |
|  ` *`shapeType`*`  | `xsd:boolean`  |A [!DNL RegionShape] value.  |
|  ` *`position`*`  | `xsd:string`  |Position in the format of the HTML `<area>` element’s [!DNL coords] attribute. For example: `coords ="0,0,84,128"`.  |
|  ` *`enabled`*`  | `xsd:boolean`  | True if image map is enabled.  |
|  ` *`lastModified`*`  | `xsd:dateTime`  | Date and time the image map was last modified.  |

