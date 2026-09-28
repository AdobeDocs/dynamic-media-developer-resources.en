---
title: Viewer SDK namespace
description: Viewer SDK namespace
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6cbf7eef-0d17-4411-9a74-22455009f66d
TQID: 'https://experienceleague.adobe.com/jP-ctDVghPscHD19iQPa4s5GnTyXKIIFOFu4UJTFo98'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Viewer SDK namespace{#viewer-sdk-namespace}

The viewer is built of many Viewer SDK components. Usually, the web page does not need to interact with the SDK components API directly; all common needs are covered in the viewer API itself.

However, some advanced use cases require that the web page reference an inner SDK component using the `getComponent()` viewer API and then use all the flexibility of the APIs of SDK itself.

The namespace that is used to load and initialize SDK components by the viewer depends on the environment in which the viewer is operating. If the viewer is running in Adobe Experience Manager, the viewer loads SDK components into `s7viewers.s7sdk` namespace. Likewise, the viewer served from Dynamic Media Classic loads the SDK into `s7classic.s7sdk`.

In either case, the namespace used by the SDK inside the viewer has either `s7viewers` or `s7classic` as the prefix. And, it is different from the plain `s7sdk` namespace used in the SDK User Guide or SDK API documentation. For that reason, it is important to use a fully qualified SDK namespace when you write custom application code that communicates with internal viewer components.

For example, if you plan to listen to `StatusEvent.NOTF_VIEW_READY` event and the viewer is served from Experience Manager, the fully qualified event type is `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`, and the event listener code looks similar to the following:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
