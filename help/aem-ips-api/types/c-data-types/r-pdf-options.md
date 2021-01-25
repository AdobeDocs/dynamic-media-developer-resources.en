---
description: PDF file options.
seo-description: PDF file options.
seo-title: PDFOptions
solution: Experience Manager
title: PDFOptions
topic: Dynamic Media Image Production System API
uuid: 7558b6b5-ad32-4baf-896b-f4e2bd48f2ec
---

# PDFOptions{#pdfoptions}

PDF file options.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`process`*`  | `xsd:string`  | Choice of "PDF processes."  |
|  `*`resolution`*`  | `xsd:double`  | File resolution.  |
|  `*`colorspace`*`  | `xsd:string`  | Post-script Colorspace Mode choice.  |
|  `*`pdfCatalog`*`  | `xsd:boolean`  | Whether to combine a multiple page PDF into an eCatalog after rendering (default is true).  |
|  `*`extractSearchWords`*`  | `xsd:boolean`  | Whether to extract search words from the PDF file.  |
|  `*`extractLinks`*`  | `xsd:boolean`  | Whether to extract PDF links into image maps assigned to the rasterized pages within IPS.  |

