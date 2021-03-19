---
description: Configuration attribute for Interactive Video Viewer.
seo-description: Configuration attribute for Interactive Video Viewer.
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
uuid: 251ab7d2-a0b5-4658-a2b8-6b39dd93dd5b
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Configuration attribute for Interactive Video Viewer.

 ` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Sets the video bitrate (in kbits per second or kbps) that is used for initial playback of video on a desktop. </p> <p>If this bitrate value does not exist in the Adaptive Video Set, the video player starts with the video that has the next lower bitrate. </p> <p>If set to <span class="codeph"> 0</span> the video player starts from the lowest possible bitrate. </p> <p>Applicable only for systems that do not have native support for HTML5 HLS video (such as Firefox, Chrome, and Internet Explorer 11 browsers on Windows 10), and when playback mode is set to auto. </p> </td> 
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

