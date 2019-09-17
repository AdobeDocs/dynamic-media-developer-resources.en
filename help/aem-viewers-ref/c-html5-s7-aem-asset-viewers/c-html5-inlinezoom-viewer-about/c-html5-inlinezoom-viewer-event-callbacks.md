---
description: null
seo-description: null
seo-title: Event callbacks
solution: Experience Manager
title: Event callbacks
topic: Dynamic media
uuid: d98074f1-7dd9-4a7f-9ef8-ebd47b698869
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

See also [FlyoutViewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-.flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e) and [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692). 
