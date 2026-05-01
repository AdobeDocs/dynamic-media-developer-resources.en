---
title: resolve
description: Debug request. This debug command parses and preprocesses the request, execute image catalog lookups, catalog Modifier inclusions, macro and variable substitutions, and so on, just like req=img.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
TQID: https://experienceleague.adobe.com/yy2WXTa9uOwqYeTjPEs-PV945VbHwy4TdnZqWJfiub0
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
# resolve{#resolve}

Debug request. This debug command parses and preprocesses the request, execute image catalog lookups, catalog::Modifier inclusions, macro and variable substitutions, and so on, just like req=img.

 `req=resolve`

The final request string is returned, instead of the result image, with MIME type `text/plain`.

The HTTP response is not cacheable.
