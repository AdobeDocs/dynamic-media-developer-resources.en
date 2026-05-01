---
description: Data file path. Relative path and name for non-image data files associated with this image.
solution: Experience Manager
title: AuxPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55f82596-72f0-48c4-9b3a-f10ea5f610f1
TQID: https://experienceleague.adobe.com/0lc0-B-gES-tjihAmUDt0EagFGbfoxEmePDce2Pn72g
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# AuxPath{#auxpath}

Data file path. Relative path and name for non-image data files associated with this image.

The server combines this value with attribute::RootPath to build the actual file path. May also be an absolute file path.

Used to specify a cabinet style file for a cabinet material or a window covering style file for a window covering material. Leave empty for all other materials.

## Properties {#section-4268350054b7421da0ce0327f0731a52}

Text string value. If specified, it must be a valid relative or absolute file path. Required for cabinet materials and window covering materials. Must be empty for all other materials.

## Default {#section-287005c2d8e948fa958f69ba7b90b437}

None.

## See also {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
