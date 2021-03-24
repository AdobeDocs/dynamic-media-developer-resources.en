---
description: Append XML to a s7 elementID.
solution: Experience Manager
title: appendElement
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
---

# appendElement{#appendelement}

Append XML to a s7:elementID.

 `appendElement.elementID=<XML>`

If a FXG node element has a `s7:elementID` defined, the `<XML>` value is appended as a child element. The `<XML>` must be encoded.

## Example {#section-4368570aa198485d91b73b4d0741478f}

Assume a `s7:elementID="group1"` attribute is defined for a Group node then the following is valid:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

This example appends a text graphic child to `group1`. 
