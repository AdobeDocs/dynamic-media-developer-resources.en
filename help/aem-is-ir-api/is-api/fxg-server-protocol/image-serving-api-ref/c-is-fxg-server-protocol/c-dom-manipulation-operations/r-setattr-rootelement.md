---
description: Set attributes to FXG Root element.
seo-description: Set attributes to FXG Root element.
seo-title: setAttr.rootElement
solution: Experience Manager
title: setAttr.rootElement
uuid: dda16612-57c7-4abe-8aa4-00e599a8ea69
feature: "Dynamic Media Classic,SDK/API"
role: "Developer,Business Practitioner"
---

# setAttr.rootElement{#setattr-rootelement}

Set attributes to FXG Root element.

 ` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

This command can manipulate attributes of the root element.

## Example {#section-2758a6e316c34b99b13b02147e5973bb}

If we have the following root element:

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

After applying the following command:

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

The root element is now changed to the following:

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">` 
