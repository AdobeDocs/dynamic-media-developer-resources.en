---
description: Image Rendering applies materials to groups or objects in vignettes.
seo-description: Image Rendering applies materials to groups or objects in vignettes.
seo-title: Materials
solution: Experience Manager
title: Materials
topic: Scene7 Image Serving - Image Rendering API
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
---

# Materials{#materials}

Image Rendering applies materials to groups or objects in vignettes.

A material consists of a set of *attributes*. Some attributes are required for certain materials, others are optional, and some are ignored if present. Many attributes have default values. Not all materials can be applied to all objects (e.g. a cabinet material cannot be applied to a sofa).

Any attributes which occur within a Material Specification Segment (MSS) but are neither listed above nor in the specific material tables below are ignored by the server.

The following tables list the basic material attributes. IR supports additional attributes for controlling [advanced render effects](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Unless otherwise noted, all material attributes are optional, with suitable default values. 
