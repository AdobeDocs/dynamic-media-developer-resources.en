---
title: SmartCropVideoPlayer.progressivebitrate
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7f9f1bfe-c68f-4ad4-a4a3-e0a8952e07af
---
# SmartCropVideoPlayer.progressivebitrate{#smartcropvideoplayer-progressivebitrate}

Configuration attribute for Smart Crop Video Viewer.

 ` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Specifies the desired video bit rate &ndash; in kilobits per second or Kbps &ndash; to play from an Adaptive Video Set in case the current system does not support adaptive video playback. </p> <p>The component picks up the video stream with the closest possible (but not exceeding) bitrate to the specified value. If all video streams in the Adaptive Video Set have higher quality than the specified value, the logic chooses the bitrate with the lowest quality. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
