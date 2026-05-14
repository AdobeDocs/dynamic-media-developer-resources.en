---
title: Command reference – Configuration attributes
description: Configuration attributes documentation for Panoramic Viewer.
solution: Experience Manager
role: Developer,User
autotag-review: '2026-05-13T22:15:11.019Z'
TQID: 'https://experienceleague.adobe.com/-6kskMStr-k7aFwy9GpQE-wjq4iAgwuEqzP2H1BWk2U'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
    internal-label: Dynamic Media Classic
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
---
# Command reference – Configuration attributes{#command-reference-configuration-attributes}

<!--
feature: Dynamic Media Classic,Viewers,SDK/API
-->

Configuration attributes documentation for Panoramic Viewer.

Any configuration command can be set in URL or using `setParam()` and/or `setParams()` API methods. Any config attribute can also be specified in server-side configuration record.

Some configuration commands may be prefixed with the class name or instance name of corresponding HTML5 SDK component. An instance name of the component is dynamic and depends on the ID of the viewer container DOM element passed to `setContainerId()` API method. Documentation includes optional prefix for such commands. For example, `vrrender` command is documented as follows:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Which means that this command is used in the following manner:

* `vrrender` (short syntax)
* `PanoramicView.vrrender` (qualified with component class name)
* `cont_panoramicView.vrrender` (qualified with component ID, assuming cont is the ID of the container element)


See [Command reference common to all viewers - Configuration attributes](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

See [Command reference common to all Viewers - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
