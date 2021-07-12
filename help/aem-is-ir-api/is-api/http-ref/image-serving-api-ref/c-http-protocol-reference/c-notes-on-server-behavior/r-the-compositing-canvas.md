---
description: If req=img, the size of the compositing canvas is determined entirely by the size of layer 0.
solution: Experience Manager
title: The compositing canvas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
---
# The compositing canvas{#the-compositing-canvas}

If req=img, the size of the compositing canvas is determined entirely by the size of layer 0.

If the `size=` for layer 0 is not specified explicitly, the layer transforms are used to calculate the size of the compositing canvas (see below).

If `req=tmb`, the size of the compositing canvas is determined by the `size=` specified for layer 0, or, if size is not specified, the compositing canvas size is set to the view rect (see below).
