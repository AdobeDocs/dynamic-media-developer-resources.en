---
description: Some applications may require a different illumination map for different kinds of materials.
solution: Experience Manager
title: Using multiple illumination maps
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a6e0be23-8b8a-4b60-aac1-c692319a0bce
---
# Using multiple illumination maps{#using-multiple-illumination-maps}

Some applications may require a different illumination map for different kinds of materials.

Up to three illumination maps can be authored for each vignette. The illumination map for a render operation is selected with the `illum=` and or `gloss=` commands.

**Default selection** If neither `illum=` nor `gloss=` are specified, the renderer will use the first authored illumination map (typically map A, aka the 'Flat' illumination map).

**Automatic selection with `gloss=`** If `illum=` is not specified or is set to -1, the renderer compares the specified `gloss=` value with the gloss values associated with each illumination map in the vignette, and choose the illumination map whose gloss value is closest to the specified `gloss=`.

**Explicit selection with `illum=`** If `illum=` is specified and set to 0, 1, or 2, the renderer will use the corresponding illumination map; `gloss=` is ignored for the purpose of selecting the illumination map.

If the vignette contains only one illumination map, the renderer will use that map and ignore the `illum=` and `gloss=` commands.
