---
description: A metadata field returned by searchAssets.
solution: Experience Manager
title: Metadata
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 62e3e215-31ea-49fd-937e-d136fdf84aff
TQID: 'https://experienceleague.adobe.com/Cdg9mW2P4YXWlpTiP9ue6cXlFjCByFiw74iJl-sCYNk'
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
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
---
# [!DNL Metadata]{#metadata}

A metadata field returned by searchAssets.

 Syntax 

## Parameters {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

|  Name  | Type  | Description  |
|---|---|---|
|  name  | `xsd:string`  | Metadata name.  |
|  value  | `xsd:string`  | Metadata value.  |
|  boolVal  | `xsd:boolean`  | Boolean metadata value (for Boolean-typed fields only).  |
|  longVal  | `xsd:long`  | Long metadata value (for int-typed fields only).  |
|  doubleVal  | `xsd:double`  | Double metadata value (for float-typed fields only).  |
|  dateVal  | `xsd:dateTime`  | Date metadata value (for date-typed fields only).  |

