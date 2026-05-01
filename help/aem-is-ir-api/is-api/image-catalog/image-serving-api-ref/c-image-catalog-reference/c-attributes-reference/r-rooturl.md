---
description: Root URL for relative image URLs. Specifies the root URL for relative image URLs.
solution: Experience Manager
title: RootUrl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72560180-53e5-4293-9dd3-c0cd196551dc
TQID: https://experienceleague.adobe.com/avHZxBI6R4N69TGWlzL-QWgUTxVcIn-ATy1BaBc90JY
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
# RootUrl{#rooturl}

Root URL for relative image URLs. Specifies the root URL for relative image URLs.

 `attribute::RootUrl` is used instead of `attribute::RootPath` when a `src=` or `mask=` value is enclosed by {curly braces} or (parentheses).

## Properties {#section-fe02269b4b724319a5d1f2cfcae31cba}

Text string value. Absolute URL root path, including the leading protocol identifier. The following protocols are supported: HTTP, HTTPS, and FTP.

## Default {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

Inherited from `default::RootUrl` if not defined. If defined but empty, relative URLs are not supported by this image catalog.

## See also {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
