---
description: Image Rendering applies materials to groups or objects in vignettes.
seo-description: Image Rendering applies materials to groups or objects in vignettes.
seo-title: Materials
solution: Experience Manager
title: Materials
topic: Scene7 Image Serving - Image Rendering API
uuid: bd02b3a8-481b-46e1-87d3-3d58daf48d2f
index: y
internal: n
snippet: y
---

# Materials{#materials}

Image Rendering applies materials to groups or objects in vignettes.

A material consists of a set of *attributes*. Some attributes are required for certain materials, others are optional, and some are ignored if present. Many attributes have default values. Not all materials can be applied to all objects (e.g. a cabinet material cannot be applied to a sofa).

Any attributes which occur within a Material Specification Segment (MSS) but are neither listed above nor in the specific material tables below are ignored by the server.

The following tables list the basic material attributes. IR supports additional attributes for controlling [advanced render effects](../../../../../../ir_api/http_protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Unless otherwise noted, all material attributes are optional, with suitable default values. 
