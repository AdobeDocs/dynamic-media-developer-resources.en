---
title: Command reference – Configuration attributes
description: Configuration attributes documentation for Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 75a9e83a-2f6e-4bfa-8881-52f8fe06f2fd
---
# Command reference – Configuration attributes{#command-reference-configuration-attributes}

Configuration attributes documentation for Video360 Viewer.

Any configuration command can be set in URL or using `setParam()`, or `setParams()`, or both, API methods. Any configuration attribute can be also specified in the server-side configuration record.

Some configuration commands may be prefixed with the class name or instance name of corresponding Viewer SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes an optional prefix for such commands. For example, `playback` command is documented as follows:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

Meaning that you can use this command in the following:

* `playback` (short syntax) 
* `VideoPlayer.playback` (qualified with component class name) 
* `cont_videoPlayer.playback` (qualified with component ID, assuming `cont` is the ID of the container element)

See also [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
