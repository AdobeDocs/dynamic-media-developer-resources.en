---
description: Options for an Adobe Illustrator file.
solution: Experience Manager
title: IllustratorOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6c06fe3-5dfa-4885-9083-c6c41ae0e0ea
TQID: 'https://experienceleague.adobe.com/I4mczv7FiGRehf8KesyWT-XtjCeRETbvMyH3Y9H-CKA'
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
# [!DNL IllustratorOptions]{#illustratoroptions}

Options for an Adobe Illustrator file.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  [!DNL process]  | `xsd:string`  | Choice of Illustrator processes.  |
|  [!DNL resolution]  | `xsd:string`  | File resolution.  |
|  colorSpace  | `xsd:string`  | Target color space.  |
|  [!DNL alpha]  | `xsd:boolean`  | Whether to rasterize the file into an image. If so, create a transparent background if the original file is defined in this way for creating overlaying logos.  |
