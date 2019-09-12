---
description: Contains information about warning or error conditions generated during a batch asset operation. The code and reason fields correspond to the fault message fields that would have been thrown for the equivalent non-batch operation.
seo-description: Contains information about warning or error conditions generated during a batch asset operation. The code and reason fields correspond to the fault message fields that would have been thrown for the equivalent non-batch operation.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Scene7 Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
index: y
internal: n
snippet: y
---

# AssetOperationFault{#assetoperationfault}

Contains information about warning or error conditions generated during a batch asset operation. The code and reason fields correspond to the fault message fields that would have been thrown for the equivalent non-batch operation.

 Syntax 

## Parameters {#section-c906f052f43e4785ba46d92b514b0923}

|  Name  | Type  | Description  |
|---|---|---|
|  ` *`assetHandle`*`  | `xsd:string`  | Asset handle for the failed operation.  |
|  ` *`code`*`  | `xsd:int`  | Operation fault code.  |
|  ` *`reason`*`  | `xsd:string`  | Fault description or reason.  |

