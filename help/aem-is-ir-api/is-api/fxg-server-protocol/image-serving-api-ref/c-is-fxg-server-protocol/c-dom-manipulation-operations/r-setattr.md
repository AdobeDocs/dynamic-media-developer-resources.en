---
title: setAttr
description: Set any attribute for a given s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
TQID: https://experienceleague.adobe.com/rbMIyWlVNKfAmgW5q-5nLVe5tPHwQjHF-JPRxJTbZ8A
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
# setAttr{#setattr}

Set any attribute for a given s7:elementID.

 `setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

If an FXG node element has a `s7:elementID` defined, you can manipulate the attributes for that node. You can set as many attribute/value pairs as you want. The attributes do not need to already be defined in the FXG but it must be valid for the node element. All values in between `{}` must be Escaped.

## Example {#section-9c37470d5f0349e5b0a97291782cb7a6}

Assume a `s7:elementID="Group1"` attribute is defined for a `BitmapGraphic` node, then the following is valid:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

This example sets the *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]*, and *[!DNL scaleY]* for the `BitmapGraphic` and overrides any existing values.
