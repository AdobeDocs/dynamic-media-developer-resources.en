---
title: VideoPlayer.progressivebitrate
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
---
# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Configuration attribute for Interactive Video Viewer.

 ` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Specifies in kilobits per seconds (kbps), the desired video bit rate to play from an Adaptive Video Set in case the current system does not support adaptive video playback. </p> <p>The component picks up the video stream with the closest possible (but not exceeding) bit rate to the specified value. If all video streams in the Adaptive Video Set have higher quality than the specified value, the logic chooses the bit rate with the lowest quality. </p> </td> 
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
