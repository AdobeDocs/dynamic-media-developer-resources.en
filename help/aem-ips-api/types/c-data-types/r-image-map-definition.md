---
description: Target definition for a click action in the browser.
seo-description: Target definition for a click action in the browser.
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
topic: Scene7 Image Production System API
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
---

# ImageMapDefinition{#imagemapdefinition}

Target definition for a click action in the browser.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  ` *`name`*`  | `xsd:string`  | The name of the image map definition.  |
|  ` *`shapeType`*`  | `xsd:string`  | One of region shape values.  |
|  ` *`region`*`  | `xsd:string`  |Image map coordinates. The format is based on the HTML `<area>` tag attributes.  |
|  ` *`action`*`  | `xsd:string`  |Other attributes to include in the HTML `<area>` tag, including the `href` URL.  |
|  ` *`enabled`*`  | `xsd:boolean`  | True if the image map is enabled.  |

