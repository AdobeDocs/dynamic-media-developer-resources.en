---
description: Preload server cache. Executes the request just like req=img, but instead of returning the image, the server returns the length of the reply image (image.length), formatted as text data with MIME type text/plain.
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
---
# loadcache{#loadcache}

Preload server cache. Executes the request just like req=img, but instead of returning the image, the server returns the length of the reply image (image.length), formatted as text data with MIME type text/plain.

 `req=loadcache`

The HTTP response is not cacheable.

Other commands in the request apply as documented.
