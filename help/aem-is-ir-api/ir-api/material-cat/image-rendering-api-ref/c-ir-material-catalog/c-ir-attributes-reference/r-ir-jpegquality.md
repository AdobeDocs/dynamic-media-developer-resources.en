---
title: JpegQuality
description: Default JPEG encoding quality. Specifies the default quality setting for JPEG-encoded reply images.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a699a9e-dbf6-4e01-95aa-37a6eb83f4df
TQID: 'https://experienceleague.adobe.com/h7SBTIJh-a1Z0e3hfMA5TSXDI3ft809TrWyCggl8loU'
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

Default JPEG encoding quality. Specifies the default quality setting for JPEG-encoded reply images.

## Properties {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

Integer number and flag, separated by a comma. The first value is in the range 1..100 and defines the quality. The second value may be `0` for normal behavior, or `1` to disable the chromaticity down-sampling employed by JPEG encoders.

## Default {#section-60900c0fb8c54444b2361513232514db}

Inherited from `default::JpegQuality` if not defined or if empty.

## See also {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
