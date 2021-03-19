---
description: Some restrictions apply for nesting and embedding.
seo-description: Some restrictions apply for nesting and embedding.
seo-title: Restrictions
solution: Experience Manager
title: Restrictions
uuid: 05e97255-db4d-4587-94d2-a7ea608ff7d4
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Restrictions{#restrictions}

Some restrictions apply for nesting and embedding.

For good server performance, the resolution of images returned by nested requests should reasonably match the texture resolution of the object(s) to which the material is being applied.

Foreign images are cached locally. Any changes to such images will be detected only after the local cache entry becomes stale (based on the expires HTTP header). 
