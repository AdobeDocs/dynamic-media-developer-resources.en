---
description: Delete any attribute for a given s7 elementID.
seo-description: Delete any attribute for a given s7 elementID.
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: bdc6fb3c-00ef-4138-8cbf-c4801e08d57c
index: y
internal: n
snippet: y
---

# deleteAttr{#deleteattr}

Delete any attribute for a given s7:elementID.

 `deleteAttr.elementID={attributeName%26attributeName}`

If an FXG node element has a `s7:elementID` defined, the attributes for that node can be deleted with this command.

## Example {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

This example removes the attributes *[!DNL x]*, *[!DNL y]*, and *[!DNL visible]* from the original FXG node. 
