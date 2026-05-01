---
title: appendElement
description: Append XML to a s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
TQID: https://experienceleague.adobe.com/AnyvEdrSx0uCu8mLp7gMRZnkOu7QNqR3VzZkW1EvwPM
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
# appendElement{#appendelement}

Append XML to a s7:elementID.

 `appendElement.elementID=<XML>`

If an FXG node element has a `s7:elementID` defined, the `<XML>` value is appended as a child element. The `<XML>` must be encoded.

## Example {#section-4368570aa198485d91b73b4d0741478f}

Assume a `s7:elementID="group1"` attribute is defined for a Group node then the following is valid:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

This example appends a text graphic child to `group1`.
