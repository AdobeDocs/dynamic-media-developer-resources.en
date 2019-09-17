---
description: null
seo-description: null
seo-title: Event callbacks
solution: Experience Manager
title: Event callbacks
topic: Dynamic media
uuid: 0c4c4111-5ad7-458c-afa2-d551b5987322
---

# Event callbacks{#event-callbacks}

The viewer supports JavaScript event callbacks that the web page uses to track the viewer initialization process or runtime behavior.

Callback handlers are assigned by passing event names and corresponding handler functions with the `handlers` property to `config` JSON object in the viewer's constructor. Alternatively, it is possible to use `setHandlers()` API method.

Supported viewer events include the following:

* `initComplete` - triggers when viewer initialization is complete and all internal components are created, so that it is possible to use `getComponent()` API. The callback handler does not take any arguments. 

* `trackEvent` - triggers each time an event occurs inside the viewer which may be handled by an event tracking system, such as Adobe Analytics. The callback handler takes the following arguments:

    * `objID {String}` not currently used. 
    * `compClass {String}` not currently used. 
    * `instName {String}` an instance name of the Viewer SDK component that triggered the event. 
    * `timeStamp {Number}` event time stamp. 
    * `eventInfo {String}` event payload.

See also [eCatalogViewer](r_html5_ecatsearch_javascriptapiref_ecatalogviewer.md#reference_BD16CADC0C054FAFB0DB4994741D47CD) and [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856). 
