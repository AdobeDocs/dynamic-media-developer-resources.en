---
description: Client cache time to live. Number of hours until expiration. Used to manage client and proxy server caching.
seo-description: Client cache time to live. Number of hours until expiration. Used to manage client and proxy server caching.
seo-title: Expiration
solution: Experience Manager
title: Expiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 3546ec40-fb31-46ed-ba43-a661ca76cdf4
index: y
internal: n
snippet: y
---

# Expiration{#expiration}

Client cache time to live. Number of hours until expiration. Used to manage client and proxy server caching.

The server calculates the expiration time/date of the NTTP response data by adding this value to the time/date of transmission.

Browsers manage caches using expiration times of files. Before passing a request to the server, the browser will check its cache to see if the file has already been down-loaded. If so, and if the file has not yet expired, the browser will send a conditional GET request (for example with the If-Modified-Since HTTP request header) rather than a normal GET request. The server has the option of responding with a '304' status and not transmitting the image. The browser will then simply load the file from its cache. This may substantially increase overall performance for frequently accessed data.

The server will set the expires HTTP response header to the current date/time plus the smallest of vignette::Expiration and all catalog::Expiration values for the vignette and all materials involved in the render operation.

The expiration is set primarily for image data responses. Certain types of responses will always be marked for immediate expiration (or tagged as non-cacheable), including all error responses or property replies.

## Properties {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Real number, -2, -1, 0, or greater. Number of hours until expiration since the response image was generated. Set to 0 to always expire the response image immediately, which effectively disables client caching. Set to -1 to mark as `never expire`. In this case the server always returns 304 status (not-modified) in response to conditional `GET` requests without checking whether the file has actually changed. Set to -2 to use the default provided by `attribute::Expiration`.

## Default {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` is used if the field is not present, if the value is -2, or if the field is empty.

## See also {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute::Expiration](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [vignette::Expiration](../../../../../ir_api/material_cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c), [req=](../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb) 
