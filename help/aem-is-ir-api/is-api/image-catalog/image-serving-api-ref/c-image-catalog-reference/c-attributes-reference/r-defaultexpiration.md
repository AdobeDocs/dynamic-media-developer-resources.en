---
description: Client cache TTL for default image responses. Provides the expiration interval for default image responses (responses which return a default image specified with either defaultImage= or attribute DefaultImage).
seo-description: Client cache TTL for default image responses. Provides the expiration interval for default image responses (responses which return a default image specified with either defaultImage= or attribute DefaultImage).
seo-title: DefaultExpiration
solution: Experience Manager
title: DefaultExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
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
