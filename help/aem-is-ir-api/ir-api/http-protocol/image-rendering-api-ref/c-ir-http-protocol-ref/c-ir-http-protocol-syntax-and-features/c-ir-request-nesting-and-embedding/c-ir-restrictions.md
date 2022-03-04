---
title: Restrictions
description: Some restrictions apply for nesting and embedding.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac2fd40b-a2f6-4f6f-9d10-3da3d701042b
---
# Restrictions{#restrictions}

Some restrictions apply for nesting and embedding.

For good server performance, the resolution of images returned by nested requests should reasonably match the texture resolution of the objects to which the material is being applied.

Foreign images are cached locally. Any changes to such images are detected only after the local cache entry becomes stale (based on the expires HTTP header).
