---
description: Thumbnail image. Requests image data formatted and sized using catalog thumbnail criteria.
seo-description: Thumbnail image. Requests image data formatted and sized using catalog thumbnail criteria.
seo-title: tmb
solution: Experience Manager
title: tmb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
index: y
internal: n
snippet: y
---

# tmb{#tmb}

Thumbnail image. Requests image data formatted and sized using catalog thumbnail criteria.

 `req=tmb`

The reply data format and response MIME type is determined by `fmt=`. Supports all commands except `fit=`.

See [Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

The HTTP response can be cached with the TTL based on `catalog::Expiration`. 
