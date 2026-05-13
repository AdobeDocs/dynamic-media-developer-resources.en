---
title: Command reference – URL
description: Command reference documentation for Smart Crop Video Viewer.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: d0797c10-2379-45f7-9e8d-a5eb56638db8
TQID: 'https://experienceleague.adobe.com/-Kguyp6buo1wFoZKPjoqI7zBaZDeWrHJDd5GklsGnCE'
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
# Command reference – URL{#command-reference-url}

Command reference documentation for Smart Crop Video Viewer.

You can set any configuration command in the URL. Or, you can use the API methods `setParam()`, or `setParams()`, or both to set any configuration command. You can also specify any config attribute in the server-side configuration record.

You can prefix some configuration commands with the class name or the instance name of corresponding Viewer SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes optional prefixes for such commands. For example, `playback` is documented as follows:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Which means that this command is used in the following manner:

* `playback` (short syntax) 
* `SmartCropVideoPlayer.playback` (qualified with component class name) 
* `cont_smartCropVideoPlayer.playback` (qualified with component ID, assuming that `cont` is the ID of the container element)

See also [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

See also [Command reference common to all Viewers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
