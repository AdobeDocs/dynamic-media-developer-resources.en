---
description: JavaScript API reference for Video360 Viewer
seo-description: JavaScript API reference for Video360 Viewer
seo-title: setVideo
solution: Experience Manager
title: setVideo
uuid: 749aa32c-c27f-476c-954b-d4524528bccc
feature: "Dynamic Media Classic,Viewers,SDK/API,360 VR Video"
role: "Developer,Business Practitioner"
---

# setVideo{#setvideo}

JavaScript API reference for Video360 Viewer

`setVideo(videoUrl)`

Sets new external video. Can be called at any time, both before and after `init()`. If called after `init()`, the viewer swaps the video in run time.

See also [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parameters {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} an absolute URL to the new video. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

None.

## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```

