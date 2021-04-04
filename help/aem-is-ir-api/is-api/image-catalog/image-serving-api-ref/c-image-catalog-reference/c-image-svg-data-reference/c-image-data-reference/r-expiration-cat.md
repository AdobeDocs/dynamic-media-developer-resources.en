---
description: Expiration
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: ee329834-a2a0-44fd-a0a5-7bf5a8e0a5a5
---
# Expiration{#expiration}

Used to manage client and proxy server caching. The server calculates the expiration time/date of the HTTP response data by adding this value to the time/date of transmission.

Browsers manage caches using expiration times of files. Before passing a request to the server, the browser checks its cache to see if the file has already been downloaded. If so, and if the file has not yet expired, the browser sends a conditional GET request (for example with the If-Modified-Since field set in the request header) rather than a normal GET request. The server has the option of responding with a '304' status and not transmitting the image. The browser then loads the file from its cache. This may substantially increase overall performance for frequently accessed data.

Expiration is used for these response types:

* `req=img` 
* `req=mask` 
* `req=tmb` 
* `req=userdata` 
* `req=map`

Certain types of responses (e.g. error responses) are always marked for immediate expiration (or tagged as non-cacheable), while others (e.g. property or default image responses) use special expiration settings ( `attribute::NonImgExpiration` and `attribute::DefaultExpiration`).

## Properties {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Real number, -2, -1, or 0 or greater. Number of hours until expiration since the response image was generated. Set to 0 to always expire the reply image immediately, which effectively disables client caching. Set to -1 to mark as *`never expire`*. In this case the server always returns 304 status (not-modified) in response to conditional GET requests without checking whether the file has actually changed. Set to -2 to use the default provided by `attribute::Expiration`.

## Default {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` is used if the field is not present, if the value is -2, or if the field is empty.

## See also {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7), [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d), [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
