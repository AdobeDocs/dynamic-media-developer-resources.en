---
description: PostScript file properties.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
TQID: https://experienceleague.adobe.com/8axLtf82SHmEyltgOhQSVoCZOACrRrqWf0gt2HOMgVo
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# [!DNL GenerationInfo]{#generationinfo}

PostScript file properties.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  [!DNL engine]  | `xsd:string`  | Generation engine used (see "Generation Info" for values).  |
|  [!DNL originator]  | `types:Asset`  | Asset record of the primary asset used in the generation.  |
|  [!DNL generated]  | `types:Asset`  | Asset record of the generated asset.  |
|  attributeArray  | `types:GenerationAttributeArray`  | Array of attributes associated with the generation process.  |
