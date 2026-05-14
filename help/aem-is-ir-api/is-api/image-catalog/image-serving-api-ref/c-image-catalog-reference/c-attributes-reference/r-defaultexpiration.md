---
description: Client cache TTL for default image responses. Provides the expiration interval for default image responses (responses which return a default image specified with either defaultImage= or attribute DefaultImage).
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
TQID: 'https://experienceleague.adobe.com/v-wtXCBtpHpf9mTjoQ58GZ9eXq-yR2tpGT0Kd-DTyNI'
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
# DefaultExpiration{#defaultexpiration}

Client cache TTL for default image responses. Provides the expiration interval for default image responses (responses which return a default image specified with either defaultImage= or attribute::DefaultImage).

Only applied when the default image is not associated with a catalog record or when the default image catalog record does not provide a specific `catalog::Expiration` value.

## Properties {#section-e564512476604fd7b964f9f2903d6d33}

Real number, 0 or greater. Number of hours until expiration since the reply data was generated. Set to 0 to always expire the reply image immediately, which effectively disables client caching for default image responses. Set to `-1` to mark as `never expire`.

## Default {#section-131cd32c2e214391857dba5af321f8cd}

Inherited from `default::DefaultExpiration` if not defined or if empty.

TTL (Time-To-Live) is the duration before the cache expires. The default TTL is 1 hour.

## See also {#section-d8642c22e3d947129367dd76366963d6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
