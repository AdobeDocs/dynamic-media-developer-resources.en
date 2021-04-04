---
description: Set text node value for s7 elementID.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
---
# setVal{#setval}

Set text node value for s7:elementID.

 `setVal.elementID= *[!DNL value]*`

If a FXG node element has a `s7:elementID` defined, the text value for that node can be manipulated.

## Example {#section-f574fd66dedd4a219aa537d7bdabea23}

Assume a `s7:elementID="paragraph1"` attribute is defined for a `TextGraphic` node then the following is valid:

`&setVal.paragraph=Hello`

This example sets the text value for the paragraph node to "Hello."
