---
title: Images
description: Image data is returned if a request successfully completes, and if the request either does not include a req= command, or if req= has one of the following values  img, debug.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
TQID: 'https://experienceleague.adobe.com/4wHyyXX0gxz9ojr5g5Puu5fBhKXo4hZDjyBuVTao3rQ'
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

Image data is returned if a request successfully completes, and if the request either does not include a req= command, or if req= has one of the following values: img, debug

The HTTP response MIME type is determined by `fmt=`, or, if `fmt=` is not specified, it depends on the value of `attribute::Format`.

The HTTP response status is '200 OK' if the request method was an unconditional `GET` or `HEAD`.

The server may reply with status '304' (not modified) and not return any image data in response to a conditional `GET` request (with the [!DNL If-Modified-Since] field present in the `request-header`).
