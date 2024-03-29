---
title: setElement
description: Set XML to a s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
---
# setElement{#setelement}

Set XML to a s7:elementID.

 `setElement.elementID=<XML>`

If an FXG node element has a `s7:elementID` defined, the `<XML>` value is replaced as a child element. The `<XML>` must be encoded.

## Example {#section-f23a998b18994dd3b5d4e1965718db9f}

Assume a `s7:elementID="group2"` attribute is defined for a `Group` node then the following is valid:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

This example removes all children from the `group2`node and replaces it with new `TextGraphic` child node.
