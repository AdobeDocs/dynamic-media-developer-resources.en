---
description: Set text node value for s7 elementID.
seo-description: Set text node value for s7 elementID.
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Scene7 Image Serving - Image Rendering API
uuid: 35b5e5b3-f395-4039-9c79-cf8b0e898fee
index: y
internal: n
snippet: y
---

# setVal{#setval}

Set text node value for s7:elementID.

 `setVal.elementID= *[!DNL value]*`

If a FXG node element has a `s7:elementID` defined, the text value for that node can be manipulated.

## Example {#section-f574fd66dedd4a219aa537d7bdabea23}

Assume a `s7:elementID="paragraph1"` attribute is defined for a `TextGraphic` node then the following is valid:

`&setVal.paragraph=Hello`

This example sets the text value for the paragraph node to "Hello." 
