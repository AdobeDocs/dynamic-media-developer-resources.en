---
description: Event callbacks
solution: Experience Manager
title: Event callbacks
topic: Dynamic Media
uuid: 325a3ccf-bae9-46f6-b3d0-70041a9548bb
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

See also [ZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-zoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) and [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643). 
