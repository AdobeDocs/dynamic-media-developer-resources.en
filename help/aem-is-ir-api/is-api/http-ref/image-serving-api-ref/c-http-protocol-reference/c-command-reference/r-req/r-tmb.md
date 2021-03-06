---
description: Thumbnail image. Requests image data formatted and sized using catalog thumbnail criteria.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
---
# tmb{#tmb}

Thumbnail image. Requests image data formatted and sized using catalog thumbnail criteria.

 `req=tmb`

The reply data format and response MIME type is determined by `fmt=`. Supports all commands except `fit=`.

See [Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

The HTTP response can be cached with the TTL based on `catalog::Expiration`.
