---
description: PostScript file options.
seo-description: PostScript file options.
seo-title: PostScriptOptions
solution: Experience Manager
title: PostScriptOptions
topic: Scene7 Image Production System API
uuid: 486dc345-c6ff-47e3-9932-416ec8d50b6b
index: y
internal: n
snippet: y
---

# PostScriptOptions{#postscriptoptions}

PostScript file options.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  ` *`process`*`  | `xsd:string`  | PostScript process choice.  |
|  ` *`resolution`*`  | `xsd:double`  | File resolution.  |
|  ` *`colorspace`*`  | `xsd:string`  | PostScript colorspace mode.  |
|  ` *`alpha`*`  | `xsd:boolean`  | Whether to rasterize the file into an image. If so, it will create a transparent background if the original file if is defined in this way. Generally used to create overlaying logos.  |
|  ` *`extractSearchWords`*`  | `xsd:boolean`  | Whether to extract search words from the PostScript file.  |

