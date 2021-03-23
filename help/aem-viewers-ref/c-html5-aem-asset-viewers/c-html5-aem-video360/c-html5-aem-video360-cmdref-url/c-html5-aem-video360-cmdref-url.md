---
description: Command reference documentation for Video360 Viewer.


solution: Experience Manager
title: Command reference – URL

feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
---

# Command reference – URL{#command-reference-url}

Command reference documentation for Video360 Viewer.

You can set any configuration command in the URL. Or, you can use the API methods `setParam()`, or `setParams()`, or both to set any configuration command. You can also specify any config attribute in the server-side configuration record.

You can prefix some configuration commands with the class name or the instance name of corresponding HTML5 Viewer SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes optional prefixes for such commands. For example, `playback` is documented as follows:

```
[Video360Player.|<containerId>_video360Player].playback
```

which means that this command is used in the following manner:

* `playback` (short syntax) 
* `Video360Player.playback` (qualified with component class name) 
* `cont_video360Player.playback` (qualified with component ID, assuming that `cont` is the ID of the container element)

See [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) and [Command reference common to all Viewers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) 
