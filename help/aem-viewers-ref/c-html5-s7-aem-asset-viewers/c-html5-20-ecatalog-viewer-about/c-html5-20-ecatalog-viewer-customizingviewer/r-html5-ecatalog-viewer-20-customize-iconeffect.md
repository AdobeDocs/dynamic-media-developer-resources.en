---
title: Icon effect
description: The zoom indicator is overlaid on the main view area. It is displayed when the image is in a reset state and it also depends on iconeffect parameter.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: fee22d02-172c-4f82-9b6c-e06db530f400
---
# Icon effect{#icon-effect}

The zoom indicator is overlaid on the main view area. It is displayed when the image is in a reset state and it also depends on iconeffect parameter.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The appearance of the viewing area is controlled with the following CSS class selector:

```
.s7ecatalogviewer .s7pageview .s7iconeffect
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS property </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Zoom indicator artwork. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position inside artwork sprite, if CSS sprites are used. </p> <p>See also <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Zoom indicator width in pixels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Zoom indicator height in pixels. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Icon effect supports the `media-type` attribute selector, which you can use to apply different icon effects on different devices. In particular, `media-type='standard'` corresponds to desktop systems where mouse input is normally used and `media-type='multitouch'` corresponds to devices with touch input.

Example - to set up a 100 x 100 pixel zoom indicator with different art for desktop systems and touch devices.

```
.s7ecatalogviewer .s7pageview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
