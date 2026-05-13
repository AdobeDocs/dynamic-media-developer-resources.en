---
title: Command reference – Configuration attributes
description: Configuration attributes documentation for Zoom Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
TQID: 'https://experienceleague.adobe.com/34VqWl1GOWOG7G8vXJIpc7NH4w26x2NOGO3yG2yknyc'
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
# Command reference – Configuration attributes{#command-reference-configuration-attributes}

Configuration attributes documentation for Zoom Viewer.

Any configuration command can be set in URL or using `setParam()`, or `setParams()`, or both, API methods. Any config attribute can also be specified in the server-side configuration record.

Some configuration commands may be prefixed with the class name or instance name of corresponding Viewer SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes an optional prefix for such commands. For example, `zoomstep` command is documented as follows:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Which means you can use the command as

* `zoomstep` (short syntax) 
* `ZoomView.zoomstep` (qualified with component class name) 
* `cont_zoomView.zoomstep` (qualified with component ID, assuming `cont` is the ID of the container element)

See also [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
