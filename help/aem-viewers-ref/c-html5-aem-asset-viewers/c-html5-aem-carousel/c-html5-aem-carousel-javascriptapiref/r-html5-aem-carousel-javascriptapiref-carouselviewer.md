---
description: JavaScript API reference for Carousel Viewer.


solution: Experience Manager
title: CarouselViewer

feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 890d869d-dbf2-4c24-88d1-34c439ab1e3a
---
# CarouselViewer{#carouselviewer}

JavaScript API reference for Carousel Viewer.

 `CarouselViewer([config])`

Constructor, creates a new HTML 5 Carousel Viewer instance.

## Parameters {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> optional JSON configuration object, allows all the viewer settings to pass to the constructor to avoid calling individual setter methods. Contains the following properties: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID of the DOM container (normally a <span class="codeph"> DIV </span>) that the viewer is inserted into. By the time this method is called, it is not necessary to have the container element created. However, the container must exist when <span class="codeph"> init() </span> is run. </p> <p>Required. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> {Object} </span> JSON object with viewer configuration parameters where the property name is either viewer-specific configuration option or SDK modifier, and the value of that property is a corresponding settings value. </p> <p>Required. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> handlers </span> - <span class="codeph"> {Object} </span> JSON object with viewer event callbacks, where the property name is the name of supported viewer event and the property value is a JavaScript function reference to appropriate callback. </p> <p>Optional. </p> <p>See <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Event callbacks </a> for more information about viewer events. </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> </p> <p> JSON object with localization data. See Localization of user interface elements and the example for more information about the object's content. </p> <p>Optional </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left" 
}, 
"fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste" 
}, 
defaultLocale:"en" 
} 
});
```
