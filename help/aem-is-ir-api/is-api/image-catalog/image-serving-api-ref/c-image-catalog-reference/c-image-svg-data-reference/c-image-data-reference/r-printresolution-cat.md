---
description: Print resolution. Print resolution for the full-size image.
solution: Experience Manager
title: PrintResolution
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2168d72a-1f2b-4833-9e6e-ba3d2ddb6d2b
TQID: https://experienceleague.adobe.com/zutuMrYBIgbLUf34ga04ZbKdwHlrBFDMPRY98M-zmTE
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
# PrintResolution{#printresolution}

Print resolution. Print resolution for the full-size image.

This value is embedded in the reply image header, unless overridden with `printRes=`.

## Properties {#section-de3c1f73da7b43208beeec841c1778c1}

Integer number, larger than 0. Expressed in dots per inch. Optional.

## Default {#section-0cac992554ec4247ab05f70d9840a045}

`attribute::PrintResolution` is used if the field is not present, if the value is 0 or if the field is empty.

## See also {#section-0593faefffe341c5ab8a4aa5da589a04}

[attribute::PrintResolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-printresolution.md#reference-a53c6850077148c9bd88a8c5c1c400c5) , [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [printRes=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-printres.md#reference-84f52afff4704c4b9d58e4bbbaea1491)
