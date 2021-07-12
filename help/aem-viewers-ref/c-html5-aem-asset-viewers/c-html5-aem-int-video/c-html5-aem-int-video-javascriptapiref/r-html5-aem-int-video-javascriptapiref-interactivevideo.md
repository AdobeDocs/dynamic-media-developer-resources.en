---
description: JavaScript API reference for Interactive Video Viewer.
solution: Experience Manager
title: InteractiveVideoViewer
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: efd0ffea-482c-4af4-ac77-ac1b7f326ce9
---
# InteractiveVideoViewer{#interactivevideoviewer}

JavaScript API reference for Interactive Video Viewer.

 `InteractiveVideoViewer([config])`

Constructor, creates a new Interactive Video Viewer instance.

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> optional JSON configuration object, allows all the viewer settings to pass to the constructor to avoid calling individual setter methods. Contains the following properties: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID of the DOM container (normally a <span class="codeph"> DIV </span>) into which the viewer is inserted. By the time this method is called, it is not necessary to have the container element created. However, the container must exist when <span class="codeph"> init() </span> is run. </p> <p>Required. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON object with viewer configuration parameters where the property name is either viewer-specific configuration option or SDK modifier, and the value of that property is a corresponding settings value. </p> <p>Required. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} </span> JSON object with viewer event callbacks, where the property name is the name of supported viewer event and the property value is a JavaScript function reference to appropriate callback. </p> <p>Optional. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Event callbacks </a> for more information about viewer events. </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> JSON object with localization data. Optional. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localization of user interface elements </a> for more information. </p> <p>See also the <i>Viewer SDK User Guide</i> and the example for more information about the object's content. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```
