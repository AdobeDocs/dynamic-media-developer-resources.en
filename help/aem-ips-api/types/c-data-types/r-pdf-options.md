---
description: PDF file options.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
TQID: https://experienceleague.adobe.com/vrPJ8y7tMNpe2P8YYJl7OpeOlEcLjJgZ--zgyinuLYE
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# [!DNL PDFOptions]{#pdfoptions}

PDF file options.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  process  | `xsd:string`  | Choice of "PDF processes."  |
|  resolution  | `xsd:double`  | File resolution.  |
|  colorspace  | `xsd:string`  | Post-script Colorspace Mode choice.  |
|  pdfCatalog  | `xsd:boolean`  | Whether to combine a multiple page PDF into an eCatalog after rendering (default is true).  |
|  extractSearchWords  | `xsd:boolean`  | Whether to extract search words from the PDF file.  |
|  extractLinks  | `xsd:boolean`  | Whether to extract PDF links into image maps assigned to the rasterized pages within IPS.  |
