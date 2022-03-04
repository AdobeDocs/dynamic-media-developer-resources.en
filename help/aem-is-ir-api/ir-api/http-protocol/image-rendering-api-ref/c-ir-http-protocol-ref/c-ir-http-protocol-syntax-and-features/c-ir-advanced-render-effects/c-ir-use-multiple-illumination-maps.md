---
title: Using multiple illumination maps
description: Some applications may require a different illumination map for different kinds of materials.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
---
# Using multiple illumination maps{#using-multiple-illumination-maps}

Some applications may require a different illumination map for different kinds of materials.

Up to three illumination maps can be authored for each vignette. The illumination map for a render operation is selected with the `illum=` and or `gloss=` commands.

**Default selection** - If `illum=` or `gloss=` are not specified, the renderer uses the first authored illumination map (typically map A, aka the 'Flat' illumination map).

**Automatic selection with `gloss=`** - If `illum=` is not specified or is set to `-1`, the renderer compares the specified `gloss=` value with the gloss values associated with each illumination map in the vignette. It chooses the illumination map whose gloss value is closest to the specified `gloss=`.

**Explicit selection with `illum=`** - If `illum=` is specified and set to `0`, `1`, or `2`, the renderer uses the corresponding illumination map; `gloss=` is ignored for selecting the illumination map.

If the vignette contains only one illumination map, the renderer uses that map and ignore the `illum=` and `gloss=` commands.
