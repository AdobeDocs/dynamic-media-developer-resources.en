---
description: Event callbacks
solution: Experience Manager
title: Event callbacks
uuid: 696838d2-11e4-4ef8-9cd3-136c5d5f6ed9
feature: "Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets"
role: "Developer,Business Practitioner"
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

See also [MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195) and [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3). 
