---
description: Set any attribute for a given s7 elementID.
seo-description: Set any attribute for a given s7 elementID.
seo-title: setAttr
solution: Experience Manager
title: setAttr
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
---

# setAttr{#setattr}

Set any attribute for a given s7:elementID.

 `setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

If a FXG node element has a `s7:elementID` defined, you can manipulate the attributes for that node. You can set as many attribute/value pairs as you want. The attributes do not need to already be defined in the FXG but it must be valid for the node element. All values in between `{}` must be Escaped.

## Example {#section-9c37470d5f0349e5b0a97291782cb7a6}

Assume a `s7:elementID="Group1"` attribute is defined for a `BitmapGraphic` node, then the following is valid:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

This example sets the *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]*, and *[!DNL scaleY]* for the `BitmapGraphic` and overrides any existing values. 
