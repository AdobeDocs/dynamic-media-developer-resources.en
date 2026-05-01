---
description: If req=img, the size of the compositing canvas is determined entirely by the size of layer 0.
solution: Experience Manager
title: The compositing canvas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
TQID: https://experienceleague.adobe.com/W97nQwmRq6O-N9cZwwaPeDZpPhNXnYUNJsE0zx9N2XU
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
# The compositing canvas{#the-compositing-canvas}

If req=img, the size of the compositing canvas is determined entirely by the size of layer 0.

If the `size=` for layer 0 is not specified explicitly, the layer transforms are used to calculate the size of the compositing canvas (see below).

If `req=tmb`, the size of the compositing canvas is determined by the `size=` specified for layer 0, or, if size is not specified, the compositing canvas size is set to the view rect (see below).
