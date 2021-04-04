---
description: URL command for Interactive Video Viewer.


solution: Experience Manager
title: interactivedata

feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
---
# interactivedata{#interactivedata}

URL command for Interactive Video Viewer.

 `interactivedata= *`file`*`

Interactive data associates certain time regions in the video content with the product data that is later displayed in interactive swatches next to the video. It is also associated in the call-to-action panel shown at the conclusion of video playback. It also provides a title for the interactive video displayed in the call-to-action panel.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies a URL or path to WebVTT interactive data content. The WebVTT file must be served by Image Serving. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

None.

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
