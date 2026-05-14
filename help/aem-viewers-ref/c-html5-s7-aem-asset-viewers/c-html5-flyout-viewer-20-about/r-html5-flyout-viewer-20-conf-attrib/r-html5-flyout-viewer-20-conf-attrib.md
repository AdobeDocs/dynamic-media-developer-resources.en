---
title: Command reference – Configuration attributes
description: Configuration attributes documentation for Flyout Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
TQID: 'https://experienceleague.adobe.com/Bus1MH5Y8xppGXxnARx0Fq11dslSbY9Q7yAlFtF6KzI'
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

Configuration attributes documentation for Flyout Viewer

You can set any configuration command in URL. Or, you can use `setParam()`, `setParams()`, or both API methods. You can also specify any configuration attribute in the server-side configuration record.

Some configuration commands are prefixed with the class name or instance name of corresponding Viewer SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes an optional prefix for such commands. For example, the `zoomfactor` command is documented as follows:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

The command is used as follows:

* `zoomfactor` (short syntax) 
* `FlyoutZoomView.zoomfactor` (qualified with a component class name) 
* `cont_flyout.zoomfactor` (qualified with the component ID, assuming that `cont` is the ID of the container element)

See also [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
