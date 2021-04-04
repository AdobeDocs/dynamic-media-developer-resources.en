---
description: Contains information about warning or error conditions generated during a batch asset operation. The code and reason fields correspond to the fault message fields that would have been thrown for the equivalent non-batch operation.
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
---
# AssetOperationFault{#assetoperationfault}

Contains information about warning or error conditions generated during a batch asset operation. The code and reason fields correspond to the fault message fields that would have been thrown for the equivalent non-batch operation.

 Syntax 

## Parameters {#section-c906f052f43e4785ba46d92b514b0923}

|  Name  | Type  | Description  |
|---|---|---|
|  `*`assetHandle`*`  | `xsd:string`  | Asset handle for the failed operation.  |
|  `*`code`*`  | `xsd:int`  | Operation fault code.  |
|  `*`reason`*`  | `xsd:string`  | Fault description or reason.  |
