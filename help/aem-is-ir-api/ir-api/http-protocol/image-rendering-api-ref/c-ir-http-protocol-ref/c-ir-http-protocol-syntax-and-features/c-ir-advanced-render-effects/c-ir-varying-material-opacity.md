---
description: Variable opacity is supported for solid color and repeatable textures applied to overlapping objects, as well as for decals and window covering materials.
solution: Experience Manager
title: Varying material opacity
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
---
# Varying material opacity{#varying-material-opacity}

Variable opacity is supported for solid color and repeatable textures applied to overlapping objects, as well as for decals and window covering materials.

Opacity information can be provided simply by using an RGB image with an alpha channel. In addition, the overall opacity can be varied with the `opacity=` command (both for RGB and RGBA images).

Wall borders also support RGBA images, primarily to support die-cut borders.

The [!DNL vnw] files which define window coverings can include an opacity channel, which is combined by the renderer with the alpha channel of the repeatable texture and the `opacity=` value to provide a full range of opacity effects for sheer and translucent window treatments.
