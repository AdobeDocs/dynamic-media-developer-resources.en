---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
topic: Dynamic Media Image Production System API
uuid: 010814a8-1d29-4b02-8449-cb26e4335e07
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

