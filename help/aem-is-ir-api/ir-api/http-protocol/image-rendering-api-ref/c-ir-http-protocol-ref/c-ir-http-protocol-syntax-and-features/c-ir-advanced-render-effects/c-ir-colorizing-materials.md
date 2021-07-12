---
description: Most materials can be colorized dynamically.
solution: Experience Manager
title: Colorizing materials
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
---
# Colorizing materials{#colorizing-materials}

Most materials can be colorized dynamically.

The colorization algorithm is quite simplistic and works best for material images which have a limited hue range. To colorize a material, the renderer simply subtracts the `bgc=` value and adds the `color=` value to each pixel value.

Colorization is disabled if `color=` is not specified. `bgc=` is ignored by cabinet materials; the base color value embedded in the [!DNL vnc] file is used instead.
