---
description: URL command for Interactive Video Viewer.
seo-description: URL command for Interactive Video Viewer.
seo-title: navigation
solution: Experience Manager
title: navigation
topic: Dynamic media
uuid: eecc7458-153c-4f36-b29e-97451f275c0c
---

# navigation{#navigation}

URL command for Interactive Video Viewer.

 ` navigation= *`file`*`

The viewer supports video chapter navigation by way of hosted WebVTT files. Cue positioning operators are not supported.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifies a URL or path to WebVTT navigation content. Image Serving should host the WebVTT file. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

None.

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.navigation.vtt,1
```

