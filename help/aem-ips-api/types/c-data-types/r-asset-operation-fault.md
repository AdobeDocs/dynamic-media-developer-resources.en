---
title: AssetOperationFault
description: Contains information about warning or error conditions generated during a batch asset operation. The code and reason fields correspond to the fault message fields that would have been thrown for the equivalent non-batch operation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
TQID: https://experienceleague.adobe.com/nXSstmzPtHLZxUnD-Px9PIaHje8KzNxSU20KKAe5E38
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# [!DNL AssetOperationFault]{#assetoperationfault}

Contains information about warning or error conditions generated during a batch asset operation. The code and reason fields correspond to the fault message fields that would have been thrown for the equivalent non-batch operation.

 Syntax 

## Parameters {#section-c906f052f43e4785ba46d92b514b0923}

|  Name  | Type  | Description  |
|---|---|---|
|  assetHandle  | `xsd:string`  | Asset handle for the failed operation.  |
|  code  | `xsd:int`  | Operation fault code.  |
|  reason  | `xsd:string`  | Fault description or reason.  |
