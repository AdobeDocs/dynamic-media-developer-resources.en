---
title: PanoramicViewer
description: Constructor, creates an HTML5 Panoramic Viewer instance.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
---
# PanoramicViewer{#panoramicviewer}

`PanoramicViewer([config])`
Constructor, creates an HTML5 Panoramic Viewer instance.

## Parameter {#section-fa807db629ce43bab286b1e1dc96c492}

config
{Object} optional JSON configuration object, lets you pass all viewer settings to the constructor and avoid calling individual setter methods. It contains the following properties:

* containerId – {String} ID of the DOM container (normally a DIV) the viewer is inserted into. It is not necessary to have the container element created by the time this method is called, however the container must exist when init() is run. Required
* params – {Object} JSON object with viewer configuration parameters where the property name is either viewer-specific configuration option or SDK modifier, and the value of that property is a corresponding settings value. Required
* handlers – {Object} JSON object with viewer event callbacks, where the property name is the name of the supported viewer event and the property value is a JavaScript function reference to the appropriate callback. See the Event Callbacks section for more information about viewer events. Optional.


## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
    "initComplete":function() {
        console.log("init complete");
}
}
});
```
