---
description: In the URL or catalog Modifier command sequence, a layer definition sequence starts with the layer= command and terminates with another layer= command, an effect= command, or the end of the URL.
seo-description: In the URL or catalog Modifier command sequence, a layer definition sequence starts with the layer= command and terminates with another layer= command, an effect= command, or the end of the URL.
seo-title: Specifying layers
solution: Experience Manager
title: Specifying layers
topic: Scene7 Image Serving - Image Rendering API
uuid: 41cd807b-2636-47d0-b0f2-c272ceaa6fe8
index: y
internal: n
snippet: y
---

# Specifying layers{#specifying-layers}

In the URL or catalog::Modifier command sequence, a layer definition sequence starts with the layer= command and terminates with another layer= command, an effect= command, or the end of the URL.

All commands within the layer definition sequence are associated with the layer.

The `layer=` command specifies a layer number, which must be an integer 0 or larger. All commands in layer definition sequences with the same layer number are applied to the same layer. If the same command occurs more than once, the last instance will prevail. 
