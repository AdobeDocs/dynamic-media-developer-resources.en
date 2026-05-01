---
title: Restrictions
description: Some restrictions apply for nesting and embedding.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
TQID: https://experienceleague.adobe.com/eUV-jgyarah5LMTaE7Ack6kEEDQZuxNf-yZr7fDB5f8
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
# Restrictions{#restrictions}

Some restrictions apply for nesting and embedding.

For good server performance, the resolution of images returned by nested requests should reasonably match the texture resolution of the objects to which the material is being applied.

Foreign images are cached locally. Any changes to such images are detected only after the local cache entry becomes stale (based on the expires HTTP header).
