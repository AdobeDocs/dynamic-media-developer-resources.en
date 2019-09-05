---
description: Set XML to a s7 elementID.
seo-description: Set XML to a s7 elementID.
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: d5b7a01a-06b8-405d-82c3-78bf353e28d4
index: y
internal: n
snippet: y
---

# setElement{#setelement}

Set XML to a s7:elementID.

 `setElement.elementID=<XML>`

If a FXG node element has a `s7:elementID` defined, the `<XML>` value is replaced as a child element. The `<XML>` must be encoded.

## Example {#section-f23a998b18994dd3b5d4e1965718db9f}

Assume a `s7:elementID="group2"` attribute is defined for a `Group` node then the following is valid:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

This example removes all children from the `group2`node and replaces it with new `TextGraphic` child node. 
