---
description: JavaScript API reference for Mixed Media Viewer.
seo-description: JavaScript API reference for Mixed Media Viewer.
seo-title: MixedMediaViewer
solution: Experience Manager
title: MixedMediaViewer
uuid: ccaabc04-a9d0-4f58-96bd-ba76e977bfac
feature: "Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets"
role: "Developer,Business Practitioner"
---

# MixedMediaViewer{#mixedmediaviewer}

JavaScript API reference for Mixed Media Viewer.

 `MixedMediaViewer([config])`

Constructor, creates a new Mixed Media Viewer instance.

## Parameters {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> optional JSON configuration object, allows all the viewer settings to pass to the constructor and avoid calling individual setter methods. Contains the following properties: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID of the DOM container (normally a <span class="codeph"> DIV </span>) that the viewer is inserted into. It is not necessary to have the container element created by the time this method is called. However, the container must exist when <span class="codeph"> init() </span> is run. Required. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON object with viewer configuration parameters where the property name is either a viewer-specific configuration option or an SDK modifier, and the value of that property is a corresponding settings value. Required. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} </span> JSON object with viewer event callbacks, where the property name is the name of supported viewer event, and the property value is a JavaScript function reference to an appropriate callback. Optional. <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local"> Event callbacks </a> for more information about viewer events. </p> </li> 
      <li id="li_C592026403804A4FAE12863944A10EE4"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Object </span>} JSON object with localization data. Optional. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Localization of user interface elements </a> for more information. </p> <p>See also the <i>Viewer SDK User Guide</i> and the example for more information about the object's content. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```

