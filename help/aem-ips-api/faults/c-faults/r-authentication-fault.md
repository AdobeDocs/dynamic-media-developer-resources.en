---
description: Thrown when a user cannot be authenticated.
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: fce5c227-9291-4d17-801f-4ef4b8d43eb4
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
