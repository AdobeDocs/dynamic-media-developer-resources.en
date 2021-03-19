---
description: Viewer SDK namespace
solution: Experience Manager
title: Viewer SDK namespace
uuid: 780396d8-e1e2-45f4-aa01-46c16e20de06
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
---

# Viewer SDK namespace{#viewer-sdk-namespace}

The viewer is built of many Viewer SDK components. In most cases, the web page does not need to interact with SDK components API directly; all common needs are covered in the viewer API itself.

However, some advanced use cases require that the web page obtain a reference to an inner SDK component using the `getComponent()` viewer API and then use all the flexibility of the APIs of SDK itself.

The namespace that is used to load and initialize SDK components by the viewer depends on the environment in which the viewer is operating. If the viewer is running in AEM (Adobe Experience Manager), the viewer loads SDK components into `s7viewers.s7sdk` namespace. And the viewer served from Dynamic Media Classic loads the SDK into `s7classic.s7sdk`.

In either case, the namespace used by the SDK inside the viewer has either `s7viewers` or `s7classic` as the prefix. And, it is different from the plain `s7sdk` namespace used in the SDK User Guide or SDK API documentation.

For that reason it is important to use a fully qualified SDK namespace when you write custom application code that communicates with internal viewer components.

For example, if you plan to listen to `StatusEvent.NOTF_VIEW_READY` event and the viewer is served from Dynamic Media Classic, the fully qualified event type is `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`, and the event listener code looks similar to the following:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

