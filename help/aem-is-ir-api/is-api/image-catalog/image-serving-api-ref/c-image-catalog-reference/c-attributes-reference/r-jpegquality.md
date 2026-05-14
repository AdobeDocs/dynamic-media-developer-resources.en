---
description: Default JPEG encoding attributes. Specifies the default attributes for JPEG reply images.
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a7f7f9-0c2c-4421-9dbc-d5c1e936f0f1
TQID: 'https://experienceleague.adobe.com/eiTYLhEUblxZFnJJf5cWgrHF4qglIYB72m-COXeGc5A'
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
# JpegQuality{#jpegquality}

Default JPEG encoding attributes. Specifies the default attributes for JPEG reply images.

## Properties {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

Integer number and flag, separated by a comma. The first value is in the range 1..100 and defines the quality. The second value may be 0 for normal behavior, or 1 to disable the RGB chromaticity down-sampling usually employed by JPEG encoders.

## Default {#section-0b25eddd59bc434abfe38eeea9d45df3}

Inherited from `default::JpegQuality` if not defined or if empty.

## See also {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
