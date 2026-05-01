---
title: Varying material opacity
description: Variable opacity is supported for solid color and repeatable textures applied to overlapping objects, as well as for decals and window-covering materials.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
TQID: https://experienceleague.adobe.com/PNC5bcZy-btKdFIacZ49WJj4optdyv2oAwwp4KVbJvM
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
# Varying material opacity{#varying-material-opacity}

Variable opacity is supported for solid color and repeatable textures applied to overlapping objects, as well as for decals and window-covering materials.

Opacity information can be provided simply by using an RGB image with an alpha channel. In addition, the overall opacity can be varied with the `opacity=` command (both for RGB and RGBA images).

Wall borders also support RGBA images, primarily to support die-cut borders.

The [!DNL vnw] files which define window-coverings can include an opacity channel. It is combined by the renderer with the alpha channel of the repeatable texture and the `opacity=` value to provide a full range of opacity effects for sheer and translucent window treatments.
