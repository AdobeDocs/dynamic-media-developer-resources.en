---
description: JavaScript API reference for Flyout Viewer.
seo-description: JavaScript API reference for Flyout Viewer.
seo-title: FlyoutViewer
solution: Experience Manager
title: FlyoutViewer
uuid: 070ae248-34fd-40fb-9d40-2c7fff388592
feature: "Dynamic Media Classic,Viewers,SDK/API,Flyout"
role: "Developer,Business Practitioner"
---

# FlyoutViewer{#flyoutviewer}

JavaScript API reference for Flyout Viewer.

 `FlyoutViewer([config])`

Constructor; creates a new Flyout Viewer instance.

## Parameters {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> optional JSON configuration object, allows all the viewer settings to pass to the constructor and avoid calling individual setter methods. Contains the following properties: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID of the DOM container (normally a <span class="codeph"> DIV </span>) that the viewer is inserted into. It is not necessary to have the container element created by the time this method is called. However, the container must exist when <span class="codeph"> init() </span> is run. Required. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON object with viewer configuration parameters where the property name is either a viewer-specific configuration option or an SDK modifier, and the value of that property is a corresponding settings value. Required. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} </span> JSON object with viewer event callbacks, where the property name is the name of supported viewer event, and the property value is a JavaScript function reference to an appropriate callback. Optional. <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> Event callbacks </a> for more information about viewer events. </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Object </span>} JSON object with localization data. Optional. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Localization of user interface elements </a> for more information. </p> <p>See the <i>Viewer SDK User Guide</i> and the example for more information about the object's content. Optional. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```

