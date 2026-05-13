---
description: Default client cache time to live. Provides a default expiration interval in case a particular catalog record does not contain a valid catalog Expiration value.
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
TQID: 'https://experienceleague.adobe.com/NkQ-Bj-gHGksaD4Tmt7k8fYVEYfe67ACo4oWS25dKOE'
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
# Expiration{#expiration}

Default client cache time to live. Provides a default expiration interval in case a particular catalog record does not contain a valid catalog::Expiration value.

## Properties {#section-063be3b2f13a48a3a5ab8080718e9812}

Real number, 0 or greater. Number of hours until expiration since the reply data was generated. Set to 0 to always expire the reply image immediately, which effectively disables client caching. Set to -1 to mark as `never expire`.

## Default {#section-f55308b195c04083996f6717c8537634}

Inherited from `default::Expiration` if not defined or if empty.

TTL (Time-To-Live) is the duration before the cache expires. The default TTL is 10 hours.

## See also {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
