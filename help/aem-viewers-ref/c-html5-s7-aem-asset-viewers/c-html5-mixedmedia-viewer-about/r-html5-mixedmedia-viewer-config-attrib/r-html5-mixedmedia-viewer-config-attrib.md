---
description: Configuration attributes documentation for Mixed Media Viewer.
seo-description: Configuration attributes documentation for Mixed Media Viewer.
seo-title: Command reference – Configuration attributes
solution: Experience Manager
title: Command reference – Configuration attributes
uuid: c0f09a05-f024-4cf0-a65f-0bfee015f635
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
---

# Command reference – Configuration attributes{#command-reference-configuration-attributes}

Configuration attributes documentation for Mixed Media Viewer.

Any configuration command can be set in URL or using `setParam()`, or `setParams()`, or both, API methods. Any config attribute can be also specified in server-side configuration record.

Some configuration commands may be prefixed with the class name or instance name of the corresponding Viewer SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes an optional prefix for such commands. For example, `zoomstep` command is documented as follows:

`[ZoomView.|<containerId>_zoomView].zoomstep`

which means that you can use this command as:

* `zoomstep` (short syntax) 
* `ZoomView.zoomstep` (qualified with component class name) 
* `cont_zoomView.zoomstep` (qualified with component ID, assuming `cont` is the ID of the container element)

See also [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 
