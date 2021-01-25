---
description: Set text node value for s7 elementID.
seo-description: Set text node value for s7 elementID.
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
---

# setVal{#setval}

Set text node value for s7:elementID.

 `setVal.elementID= *[!DNL value]*`

If a FXG node element has a `s7:elementID` defined, the text value for that node can be manipulated.

## Example {#section-f574fd66dedd4a219aa537d7bdabea23}

Assume a `s7:elementID="paragraph1"` attribute is defined for a `TextGraphic` node then the following is valid:

`&setVal.paragraph=Hello`

This example sets the text value for the paragraph node to "Hello." 
