---
description: Client cache time to live. Number of hours until expiration. Used to manage client and proxy server caching.
seo-description: Client cache time to live. Number of hours until expiration. Used to manage client and proxy server caching.
seo-title: Expiration
solution: Experience Manager
title: Expiration
topic: Dynamic Media Image Serving - Image Rendering API
uuid: fa267728-9a36-4705-97d6-d567148fc2d7
---

# Expiration{#expiration}

Client cache time to live. Number of hours until expiration. Used to manage client and proxy server caching.

See ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)` for details.

## Properties {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Real number, -2, -1, 0, or greater. Number of hours until expiration since the response image was generated. Set to 0 to always expire the response image immediately, which effectively disables client caching. Set to -1 to mark as `never expire`; in this case the server always returns 403 status in response to conditional `GET` requests without checking whether the file has actually changed. Set to -2 to use the default provided by `attribute::Expiration`.

## Default {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` is used if the field is not present, if the value is -2, or if the field is empty.

## See also {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb) 
