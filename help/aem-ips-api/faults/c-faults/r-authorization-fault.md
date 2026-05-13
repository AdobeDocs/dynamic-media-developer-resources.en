---
description: Thrown when an authenticated user has insufficient permissions to accomplish a task.
solution: Experience Manager
title: authorizationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 76965735-92d8-46be-b589-67cad3b987dc
TQID: 'https://experienceleague.adobe.com/oDM8k3LLSl2AD8i2vtLirkHl9J5pz8PxzgMjKLCl7do'
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
# authorizationFault{#authorizationfault}

Thrown when an authenticated user has insufficient permissions to accomplish a task.

 Syntax 

## Fault Types {#section-1f04dec489714ee6bb7256fae6ab7730}

|  ID  | Fault  |
|---|---|
|  20000  | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY`  |
|  20001  | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME`  |
|  20002  | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER`  |
|  20003  | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION`  |
|  20004  | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION`  |
|  20005  | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE`  |
|  20006  | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY`  |
|  20007  | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER`  |
|  20008  | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP`  |
|  20009  | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION`  |

## Fault Fields {#section-4e3e41f41fea402a9ae314bfd05f663e}

|  Name  | Type  | Description  |
|---|---|---|
|  `code`  | `xsd:int`  | Fault ID  |
|  `reason`  | `xsd:string`  | An informative message describing the fault.  |
