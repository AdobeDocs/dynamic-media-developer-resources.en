---
title: RootUrl
description: Root URL for relative image URLs. Specifies the root URL for relative image URLs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
TQID: 'https://experienceleague.adobe.com/1wKgvbd1t4HyDlz-CTDkp2gQuryBJYfMyDG7SmVgNwE'
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
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
---
# RootUrl{#rooturl}

Root URL for relative image URLs. Specifies the root URL for relative image URLs. The`attribute::RootUrl` is used instead of `attribute::RootPath` when a `src=` value is enclosed by { curly braces }.

## Properties {#section-69cd0f71ea614770a8778c745d23197a}

Text string value. Absolute URL root path, including the leading protocol identifier. The following protocols are supported: HTTP, HTTPS, and FTP.

## Default {#section-7a81569728474725a70f3a2cc4d48e85}

Inherited from `default::RootUrl` if not defined. If defined but empty, relative URLs are not supported by this material catalog.

## See also {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
