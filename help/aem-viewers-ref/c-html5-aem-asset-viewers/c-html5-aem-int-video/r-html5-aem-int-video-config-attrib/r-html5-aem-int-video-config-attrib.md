---
title: Command reference – Configuration attributes
description: Configuration attributes documentation for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 80b7971c-82dc-47a2-adde-9e061a0f856d
TQID: https://experienceleague.adobe.com/HgqgxMgHqsb4h3WAFSlS9V-muD6eZQpoW94y1uN4HnU
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Command reference – Configuration attributes{#command-reference-configuration-attributes}

Configuration attributes documentation for Interactive Video Viewer.

Any configuration command can be set in URL or using `setParam()`, or `setParams()`, or both, API methods. Any config attribute can also be specified in the server-side configuration record.

Some configuration commands may be prefixed with the class name or instance name of corresponding Viewer SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes an optional prefix for such commands. For example, `playback` command is documented as follows:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

And means that you can use the following command as:

* `playback` (short syntax) 
* `VideoPlayer.playback` (qualified with component class name) 
* `cont_videoPlayer.playback` (qualified with component ID, assuming `cont` is the ID of the container element)

See also [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
