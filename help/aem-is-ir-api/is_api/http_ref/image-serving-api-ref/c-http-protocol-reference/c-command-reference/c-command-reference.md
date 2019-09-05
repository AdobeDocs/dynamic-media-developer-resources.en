---
description: This section describes the HTTP protocol commands.
seo-description: This section describes the HTTP protocol commands.
seo-title: Command reference
solution: Experience Manager
title: Command reference
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e15b99c-e300-4c3d-90f1-1210eabc4f5b
index: y
internal: n
snippet: y
---

# Command reference{#command-reference}

This section describes the HTTP protocol commands.

**For Dynamic Media in AEM only**: Beyond the basic image settings that are available in the user interface, [!DNL Dynamic Media] in AEM ( [!DNL Adobe Experience Manager]) supports numerous advanced image modifications that you can specify in the **Image Modifiers** field. These parameters are defined below. Be aware, however, that the following functionality is not supported in Dynamic Media in AEM.

* Color correction commands: `icc=` and `iccEmbed=`. 
* Basic templating and text rendering commands: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` and `textPs=`. 
* Localization commands: `locale=` and `req=xlate`. 
* `req=set` is not available for general usage. 
* `req=mbrset` 
* `req=saveToFile` 
* `req=targets` 
* `template=` 
* Non-core Dynamic Media services: SVG, Image Rendering, and Web-to-Print.

See also the Dynamic Media [Image Preset Options](https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/dynamic-media/image-presets.html#Image%20Preset%20Options) in the AEM 6.2 documentation. 
