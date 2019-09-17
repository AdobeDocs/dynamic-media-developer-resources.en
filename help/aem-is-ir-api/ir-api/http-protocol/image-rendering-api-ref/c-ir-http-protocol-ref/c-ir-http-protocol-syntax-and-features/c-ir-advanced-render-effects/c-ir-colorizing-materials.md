---
description: Most materials can be colorized dynamically.
seo-description: Most materials can be colorized dynamically.
seo-title: Colorizing materials
solution: Experience Manager
title: Colorizing materials
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
---

# Colorizing materials{#colorizing-materials}

Most materials can be colorized dynamically.

The colorization algorithm is quite simplistic and works best for material images which have a limited hue range. To colorize a material, the renderer simply subtracts the `bgc=` value and adds the `color=` value to each pixel value.

Colorization is disabled if `color=` is not specified. `bgc=` is ignored by cabinet materials; the base color value embedded in the [!DNL vnc] file is used instead. 
