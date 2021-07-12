---
description: Reply image size limit. Maximum reply image width and height that may be returned to the client.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
---
# MaxPix{#maxpix}

Reply image size limit. Maximum reply image width and height that may be returned to the client.

The server returns an error if a request would cause a reply image whose width and/or height is larger than `attribute::MaxSize`.

## Properties {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Two integer numbers, larger than 0, separated by a comma. Width and height in pixels. May also be set to 0,0 to permit any reply image size with no limitations.

## Default {#section-45b38dc661854d11b97df5709f4f3434}

Inherited from default::MaxPix if not defined or if empty.

## See also {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
