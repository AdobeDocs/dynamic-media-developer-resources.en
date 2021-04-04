---
description: PostScript file options.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
---
# PostScriptOptions{#postscriptoptions}

PostScript file options.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`process`*`  | `xsd:string`  | PostScript process choice.  |
|  `*`resolution`*`  | `xsd:double`  | File resolution.  |
|  `*`colorspace`*`  | `xsd:string`  | PostScript colorspace mode.  |
|  `*`alpha`*`  | `xsd:boolean`  | Whether to rasterize the file into an image. If so, it will create a transparent background if the original file if is defined in this way. Generally used to create overlaying logos.  |
|  `*`extractSearchWords`*`  | `xsd:boolean`  | Whether to extract search words from the PostScript file.  |
