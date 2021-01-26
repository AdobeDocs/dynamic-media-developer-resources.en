---
description: Command reference documentation for Interactive Video Viewer.
seo-description: Command reference documentation for Interactive Video Viewer.
seo-title: Command reference – URL
solution: Experience Manager
title: Command reference – URL
topic: Dynamic Media
uuid: 4f9e4a79-6865-4e41-b30b-84ff2c6f6045
---

# Command reference – URL{#command-reference-url}

Command reference documentation for Interactive Video Viewer.

You can set any configuration command in the URL. Or, you can use the API methods `setParam()`, or `setParams()`, or both to set any configuration command. You can also specify any config attribute in the server-side configuration record.

You can prefix some configuration commands with the class name or the instance name of corresponding Viewer SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes optional prefixes for such commands. For example, `playback` is documented as follows:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

which means that this command is used in the following manner:

* `playback` (short syntax) 
* `VideoPlayer.playback` (qualified with component class name) 
* `cont_videoPlayer.playback` (qualified with component ID, assuming that `cont` is the ID of the container element)

See also [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

See also [Command reference common to all Viewers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226). 
