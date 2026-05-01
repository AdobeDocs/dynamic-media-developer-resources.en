---
description: Delete any attribute for a given s7 elementID.
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
TQID: https://experienceleague.adobe.com/4ltrp4Qu5tA1m-NPL4bdp4IJDAI5hdF6Rr1A2MbTvbg
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
# deleteAttr{#deleteattr}

Delete any attribute for a given s7:elementID.

 `deleteAttr.elementID={attributeName%26attributeName}`

If an FXG node element has a `s7:elementID` defined, the attributes for that node can be deleted with this command.

## Example {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

This example removes the attributes *[!DNL x]*, *[!DNL y]*, and *[!DNL visible]* from the original FXG node.
