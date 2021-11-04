---
title: SmartCropVideoPlayer.playback
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id:
---
# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Configuration attribute for Smart Crop Video Viewer.

 `[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Sets the type of playback used by the viewer. When <span class="codeph"> auto</span> is set, on most desktop browsers and all iOS devices, the viewer uses HTML5 streaming video in HLS format. It falls back to progressive HTML5 playback on certain systems like older Internet Explorer and Android™. </p> <p>If <span class="codeph"> progressive</span> is specified, the viewer relies only on HTML5 playback as natively supported by browsers and plays video progressively on all systems. </p> <p>For more information on the playback selection in auto and progressive modes, consult the Viewer SDK User Guide. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

Ignored when viewer works with external video. See [External Video Support]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
