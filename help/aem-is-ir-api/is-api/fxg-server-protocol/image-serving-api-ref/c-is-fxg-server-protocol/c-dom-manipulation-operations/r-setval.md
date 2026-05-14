---
title: setVal
description: Set the text node value for s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
TQID: 'https://experienceleague.adobe.com/bwE12rWee56rVQDuctPsmq5TUwVJy39HNUff-ZYuybM'
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
# setVal{#setval}

Set the text node value for s7:elementID.

 `setVal.elementID= *[!DNL value]*`

If an FXG node element has a `s7:elementID` defined, the text value for that node can be manipulated.

## Example {#section-f574fd66dedd4a219aa537d7bdabea23}

Assume a `s7:elementID="paragraph1"` attribute is defined for a `TextGraphic` node then the following is valid:

`&setVal.paragraph=Hello`

This example sets the text value for the paragraph node to "Hello."
