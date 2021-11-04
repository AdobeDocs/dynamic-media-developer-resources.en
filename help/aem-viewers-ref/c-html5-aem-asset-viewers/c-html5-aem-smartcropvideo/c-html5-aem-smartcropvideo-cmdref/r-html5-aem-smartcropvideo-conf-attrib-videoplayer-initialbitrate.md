---
title: SmartCropVideoPlayer.initialbitrate
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
---
# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

Configuration attribute for Video Viewer.

 ` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>Sets the video bitrate &ndash; in kilobits per seconds or Kbps &ndash; that is used for initial playback of video on desktops. </p> <p>If this bitrate value does not exist in the Adaptive Video Set, then the video player starts the video that has the next lowest bitrate. </p> <p>If set to <span class="codeph"> 0 </span>, the video player starts from the lowest possible bitrate. Applicable only for systems that do not have native support for HTML5 HLS video (which are Firefox, Chrome and Internet Explorer 11 browsers on Windows 10), and when playback mode is set to <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
