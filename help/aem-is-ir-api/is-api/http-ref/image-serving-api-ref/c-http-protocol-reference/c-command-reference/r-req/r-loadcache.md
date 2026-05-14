---
description: Preload server cache. Executes the request just like req=img, but instead of returning the image, the server returns the length of the reply image (image.length), formatted as text data with MIME type text/plain.
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
TQID: 'https://experienceleague.adobe.com/Llp-0huLGkxBVxSgRngyAtNKqeHuZ02xJu71MM-Nqww'
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
# loadcache{#loadcache}

Preload server cache. Executes the request just like req=img, but instead of returning the image, the server returns the length of the reply image (image.length), formatted as text data with MIME type text/plain.

 `req=loadcache`

The HTTP response is not cacheable.

Other commands in the request apply as documented.
