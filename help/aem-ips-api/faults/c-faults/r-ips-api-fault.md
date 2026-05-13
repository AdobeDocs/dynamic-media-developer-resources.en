---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 48be47f6-4c1c-4f19-afa7-f643e504c287
TQID: 'https://experienceleague.adobe.com/1gvR4HmnB6XVkcWsSKNFRONPAxbYEItcdQqbSv3E0S0'
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
# ipsApiFault{#ipsapifault}

 Syntax 

## Fault Types {#section-425697675cac4b2ab5c48bd463956401}

|  ID  | Fault  |
|---|---|
|  30000  | `IPS_API_FAULT_CODE_EXCEPTION`  |
|  30001  | `IPS_API_FAULT_CODE_INVALID_PARAMETER`  |
|  30002  | `IPS_API_FAULT_CODE_MISSING_PARAMETER`  |
|  30003  | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML`  |

## Fault Fields {#section-37fe1aef1d5f4ca480071ca933aba826}

|  Name  | Type  | Description  |
|---|---|---|
|  `code`  | `xsd:int`  | Fault ID  |
|  `reason`  | `xsd:string`  | An informative message describing the fault.  |
