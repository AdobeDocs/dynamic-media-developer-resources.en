---
title: Command reference – Configuration attributes
description: Configuration attributes documentation for Panoramic Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
---
# Command reference – Configuration attributes{#command-reference-configuration-attributes}

Configuration attributes documentation for Panoramic Viewer.

Any configuration command can be set in URL or using `setParam()` and/or `setParams()` API methods. Any config attribute can be also specified in server-side configuration record.

Some configuration commands may be prefixed with the class name or instance name of corresponding HTML5 SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation will include optional prefix for such commands. For example, `vrrender` command is documented as follows:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Which means that this command is used in the following manner:

* `vrrender` (short syntax)
* `PanoramicView.vrrender` (qualified with component class name)
* `cont_panoramicView.vrrender` (qualified with component ID, assuming cont is the ID of the container element)


See [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

See [Command reference common to all Viewers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
