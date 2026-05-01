---
description: Thumbnail image. Requests image data formatted and sized using catalog thumbnail criteria.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
TQID: https://experienceleague.adobe.com/TYsb8byIsSpNCC5E695GI3SiFc49vMyBMAGWZlHqb90
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
# tmb{#tmb}

Thumbnail image. Requests image data formatted and sized using catalog thumbnail criteria.

 `req=tmb`

The reply data format and response MIME type is determined by `fmt=`. Supports all commands except `fit=`.

See [Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

The HTTP response can be cached with the TTL based on `catalog::Expiration`.
