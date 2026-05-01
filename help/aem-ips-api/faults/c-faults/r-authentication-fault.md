---
description: Thrown when a user cannot be authenticated.
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fce5c227-9291-4d17-801f-4ef4b8d43eb4
TQID: https://experienceleague.adobe.com/kYWkSAX5B2HgXvLQ1G-TUbM1P01-eBg4dFJGiJVNWdc
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# authenticationFault{#authenticationfault}

Thrown when a user cannot be authenticated.

 Syntax

## Fault Types {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

|  ID  | Fault  |
|---|---|
|  10000  | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS`  |
|  10001  | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS`  |
|  10002  | `AUTHENTICATION_FAULT_CODE_INVALID_USER`  |

## Fault Fields {#section-1fe84846a7154b03ab49552810ee9ac3}

|  Name  | Type  | Description  |
|---|---|---|
|  `code`  | `xsd:int`  | Fault ID  |
|  `reason`  | `xsd:string`  | An informative message describing the fault.  |
