---
description: Some restrictions apply for nesting and embedding.


solution: Experience Manager
title: Restrictions

feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# Restrictions{#restrictions}

Some restrictions apply for nesting and embedding.

For good server performance, the resolution of images returned by nested requests should reasonably match the texture resolution of the object(s) to which the material is being applied.

Foreign images are cached locally. Any changes to such images will be detected only after the local cache entry becomes stale (based on the expires HTTP header). 
