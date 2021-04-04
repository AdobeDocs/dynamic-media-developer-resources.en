---
description: Image data is returned if a request successfully completes, and if the request either does not include a req= command, or if req=img or req=tmb.
solution: Experience Manager
title: Images
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
---
# Images{#images}

Image data is returned if a request successfully completes, and if the request either does not include a req= command, or if req=img or req=tmb.

The HTTP response MIME type is determined by `fmt=`, or, if `fmt=` is not specified, it is `<image/jpeg>`.

The HTTP response status is '200 OK' if the request method was an unconditional `GET` or `HEAD`.

The server may reply with status '304' (not modified) and not return any image data in response to a conditional `GET` request (which includes a valid `If-Modified-Since` or `If-None-Match` header).
