---
description: In the URL or catalog Modifier command sequence, a layer definition sequence starts with the layer= command and terminates with another layer= command, an effect= command, or the end of the URL.
solution: Experience Manager
title: Specifying layers
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bedd5dac-7577-4c8a-9dc3-43aa4438e53a
TQID: https://experienceleague.adobe.com/FPe4WKQAQm9rmpQTD-cDA7vN0ey-Gsney1l6czRHbtA
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
# Specifying layers{#specifying-layers}

In the URL or catalog::Modifier command sequence, a layer definition sequence starts with the layer= command and terminates with another layer= command, an effect= command, or the end of the URL.

All commands within the layer definition sequence are associated with the layer.

The `layer=` command specifies a layer number, which must be an integer 0 or larger. All commands in layer definition sequences with the same layer number are applied to the same layer. If the same command occurs more than once, the last instance prevails.
