---
description: Reply image size limit. Maximum reply image width and height that may be returned to the client.
seo-description: Reply image size limit. Maximum reply image width and height that may be returned to the client.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
---

# MaxPix{#maxpix}

Reply image size limit. Maximum reply image width and height that may be returned to the client.

The server returns an error if a request would cause a reply image whose width or height is larger than `attribute::MaxPix`.

## Properties {#section-b175425b9e9f48e0b1a71640f6a9e936}

Two integer numbers, larger than 0, separated by a comma. Width and height in pixels. May also be set to `0,0` to permit any reply image size with no limitations.

## Default {#section-1003537434da432fb2af100ecdbf9d72}

Inherited from `default::MaxPix` if not defined or if empty.

## See also {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) 
