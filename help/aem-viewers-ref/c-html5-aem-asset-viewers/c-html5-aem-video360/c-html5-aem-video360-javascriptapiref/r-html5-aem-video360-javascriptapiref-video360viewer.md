---
description: JavaScript API reference for Video360 Viewer.
seo-description: JavaScript API reference for Video360 Viewer.
seo-title: Video360Viewer
solution: Experience Manager
title: Video360Viewer
topic: Dynamic Media
uuid: b5d5e270-687c-40aa-9de4-c5bc2a7806f7
---

# Video360Viewer{#video-viewer}

JavaScript API reference for Video360 Viewer.

 `Video360Viewer([config])`

Constructor, creates a new HTML5 Video360 Viewer instance.

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> optional JSON configuration object, allows all the viewer settings to pass to the constructor to avoid calling individual setter methods. Contains the following properties: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID of the DOM container (normally a <span class="codeph"> DIV </span>) into which the viewer is inserted. By the time this method is called, it is not necessary to have the container element created. However, the container must exist when <span class="codeph"> init() </span> is run. </p> <p>Required. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON object with viewer configuration parameters where the property name is either viewer-specific configuration option or SDK modifier, and the value of that property is a corresponding settings value. </p> <p>Required. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} </span> JSON object with viewer event callbacks, where the property name is the name of supported viewer event and the property value is a JavaScript function reference to appropriate callback. </p> <p>Optional. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Event callbacks </a> for more information about viewer events. </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> JSON object with localization data. Optional. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Localization of user interface elements </a> for more information. </p> <p>See also the <i>Viewer SDK User Guide</i> and the example for more information about the object's content. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```

