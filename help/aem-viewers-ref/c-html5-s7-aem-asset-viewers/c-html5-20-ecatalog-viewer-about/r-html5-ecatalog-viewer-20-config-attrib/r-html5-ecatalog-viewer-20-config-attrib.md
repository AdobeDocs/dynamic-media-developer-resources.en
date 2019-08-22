---
description: Configuration attributes documentation for eCatalog Viewer.
seo-description: Configuration attributes documentation for eCatalog Viewer.
seo-title: Command reference – Configuration attributes
solution: Experience Manager
title: Command reference – Configuration attributes
topic: Dynamic media
uuid: 823ad411-653a-44de-97de-147e3b27a917
index: y
internal: n
snippet: y
---

# Command reference – Configuration attributes{#command-reference-configuration-attributes}

Configuration attributes documentation for eCatalog Viewer.

Any configuration command can be set in URL or using `setParam()`, or `setParams()`, or both, API methods. You can also specify any configuration attribute that is specified in the server-side configuration record.

For some configuration commands you can prefix them with the class name or instance name of corresponding Viewer SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes optional prefix for such commands. For example, `zoomstep` command is documented as follows:

`[PageView.|<containerId>_pageView].zoomstep`

which means that you can use this command as:

* `zoomstep` (short syntax) 
* `PageView.zoomstep` (qualified with component class name) 
* `cont_pageView.zoomstep` (qualified with component ID, assuming `cont` is the ID of the container element)

See also [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 