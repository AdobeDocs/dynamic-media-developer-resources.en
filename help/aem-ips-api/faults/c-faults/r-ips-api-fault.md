---
description: null
seo-description: null
seo-title: ipsApiFault
solution: Experience Manager
title: ipsApiFault
topic: Scene7 Image Production System API
uuid: d2ccab10-29f0-4961-8e6d-a56b30b836d5
index: y
internal: n
snippet: y
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

