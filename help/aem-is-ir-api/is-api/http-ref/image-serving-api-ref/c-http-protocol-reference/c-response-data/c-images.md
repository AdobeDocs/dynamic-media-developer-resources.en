---
description: Image data is returned if a request successfully completes, and if the request either does not include a req= command, or if req=img or req=tmb.
solution: Experience Manager
title: Images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
TQID: https://experienceleague.adobe.com/sMXAWM1CuaAO7BcdW7jRJ8ZzZvyMcFT9KQOzveB-t2E
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
# Images{#images}

Image data is returned if a request successfully completes, and if the request either does not include a req= command, or if req=img or req=tmb.

The HTTP response MIME type is determined by `fmt=`, or, if `fmt=` is not specified, it is `<image/jpeg>`.

The HTTP response status is '200 OK' if the request method was an unconditional `GET` or `HEAD`.

The server may reply with status '304' (not modified) and not return any image data in response to a conditional `GET` request (which includes a valid `If-Modified-Since` or `If-None-Match` header).
