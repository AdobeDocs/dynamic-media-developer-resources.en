---
description: Client cache TTL for non-image responses. Provides the expiration interval for certain non-image responses.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
TQID: 'https://experienceleague.adobe.com/A21KkwsYFIMp9Pw0WyX-c-3UVlFg2FacObh2jjRVTwA'
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
# NonImgExpiration{#nonimgexpiration}

Client cache TTL for non-image responses. Provides the expiration interval for certain non-image responses.

Provides the expiration interval for certain non-image responses, including those sent in response to the following commands:

* `req=imageset` 
* `req=catalogprops` 
* `req=exists` 
* `req=imageprops` 
* `req=props`

## Properties {#section-d37e3113f4b1468b86b5a14e80d94c83}

Real number, 0 or greater. Number of hours until expiration since the reply data was generated. Set to 0 to always expire the reply image immediately, which effectively disables client caching for default image responses. Set to -1 to mark as *never expire*.

## Default {#section-96981360c0234b7f824d2ff7c25a7954}

Inherited from `default::NonImgExpiration` if not defined or if empty.

TTL (Time-To-Live) is the duration before the cache expires. The default TTL is 6 minutes.

## See also {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
