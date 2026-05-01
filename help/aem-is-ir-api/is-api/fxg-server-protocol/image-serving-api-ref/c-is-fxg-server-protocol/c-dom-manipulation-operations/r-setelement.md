---
title: setElement
description: Set XML to a s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
TQID: https://experienceleague.adobe.com/MuKImLy1ZuP63eJ1UnVnKCSDvGv2eMx1zQNANO51D48
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# setElement{#setelement}

Set XML to a s7:elementID.

 `setElement.elementID=<XML>`

If an FXG node element has a `s7:elementID` defined, the `<XML>` value is replaced as a child element. The `<XML>` must be encoded.

## Example {#section-f23a998b18994dd3b5d4e1965718db9f}

Assume a `s7:elementID="group2"` attribute is defined for a `Group` node then the following is valid:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

This example removes all children from the `group2`node and replaces it with new `TextGraphic` child node.
