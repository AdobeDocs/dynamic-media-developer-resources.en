---
title: Command reference – Configuration attributes
description: Configuration attributes documentation for Flyout Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
---
# Command reference – Configuration attributes{#command-reference-configuration-attributes}

Configuration attributes documentation for Flyout Viewer

You can set any configuration command in URL. Or, you can use `setParam()`, `setParams()`, or both API methods. You can also specify any configuration attribute in the server-side configuration record.

Some configuration commands are prefixed with the class name or instance name of corresponding Viewer SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes an optional prefix for such commands. For example, the `zoomfactor` command is documented as follows:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

The command is used as follows:

* `zoomfactor` (short syntax) 
* `FlyoutZoomView.zoomfactor` (qualified with a component class name) 
* `cont_flyout.zoomfactor` (qualified with the component ID, assuming that `cont` is the ID of the container element)

See also [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
