---
description: PostScript file options.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
TQID: https://experienceleague.adobe.com/6qxyY4LnonK-taI0nlzGTLyInn8jxyFl9J-TOMBzMSc
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# [!DNL PostScriptOptions]{#postscriptoptions}

PostScript file options.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  process  | `xsd:string`  | PostScript process choice.  |
|  resolution  | `xsd:double`  | File resolution.  |
|  colorspace  | `xsd:string`  | PostScript colorspace mode.  |
|  alpha  | `xsd:boolean`  | Whether to rasterize the file into an image. If so, it creates a transparent background if the original file if is defined in this way. Generally used to create overlaying logos.  |
|  extractSearchWords  | `xsd:boolean`  | Whether to extract search words from the PostScript file.  |
