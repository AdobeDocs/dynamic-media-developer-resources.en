---
description: Configuration attributes documentation for Spin Viewer.


solution: Experience Manager
title: Command reference – Configuration attributes

feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
---
# Command reference – Configuration attributes{#command-reference-configuration-attributes}

Configuration attributes documentation for Spin Viewer.

Any configuration command can be set in URL or using `setParam()`, or `setParams()`, or both, API methods. Any config attribute can be also specified in server-side configuration record.

Some configuration commands may be prefixed with the class name or instance name of corresponding Viewer SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes an optional prefix for such commands. For example, `zoomstep` command is documented as follows:

`[SpinView.|<containerId>_spinView].zoomstep`

which means that you can use this command as:

* `zoomstep` (short syntax) 
* `SpinView.zoomstep` (qualified with component class name) 
* `cont_spinView.zoomstep` (qualified with component ID, assuming `cont` is the ID of the container element)

See also [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
