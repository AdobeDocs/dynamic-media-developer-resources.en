---
description: Vignette file path. Relative path and name of a vignette file.
solution: Experience Manager
title: Path
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5562b0e0-0476-4dd0-acce-058601b9af0a
TQID: 'https://experienceleague.adobe.com/70KfRxztxkghF-HS5uK-wPIelm-XGRF0ywyYnWxWNAw'
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
# Path{#path}

Vignette file path. Relative path and name of a vignette file.

The server combines this value with `attribute::RootPath` to build the actual vignette file path. May also be an absolute path.

## Properties {#section-b3b295feac084b56bd8a153c04987153}

Text string. Optional. If specified, it must be a valid relative or absolute file path. If empty, `vignette::Modifier` must include the `vignette=` command.

## Default {#section-a1d2133856084eb79a5be8230a4b38fd}

None.

## See also {#section-177131dad5804964bfb8957c1f6e5191}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
