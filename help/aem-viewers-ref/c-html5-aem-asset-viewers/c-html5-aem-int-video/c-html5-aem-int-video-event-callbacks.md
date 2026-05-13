---
title: Event callbacks
description: Event callbacks
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
TQID: 'https://experienceleague.adobe.com/pAXI43BvGyX7rM3--kuoLsAsexeM993-WKoLPCU9Zzg'
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

* `quickViewActivate` - triggers when a user clicks or taps on interactive swatch within the interactive swatches component or in the "call to action" screen shown in the end of video playback. Callback handler takes the only argument which is a JSON object with the following fields:

  * `sku` { `String`} SKU value that is associated with the interactive swatch. 
  * `<additionalVariable>` { `String`} zero or more additional variables associated with the interactive swatch.

See also [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) and [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
