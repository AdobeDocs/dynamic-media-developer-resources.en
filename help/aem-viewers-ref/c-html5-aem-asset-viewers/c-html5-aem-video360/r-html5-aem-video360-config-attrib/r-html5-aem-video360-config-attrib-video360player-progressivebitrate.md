---
title: Video360Player.progressivebitrate
description: Configuration attribute for Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
TQID: https://experienceleague.adobe.com/RyY-ct49Ic2-TPgx6e3fnwWUKiPDYgduMEbmBpW4bso
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Configuration attribute for Video360 Viewer.

 ` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Specifies the desired video bit rate (in kilobits per second or kbps) to play from an Adaptive Video Set in case the current system does not support adaptive video playback. </p> <p>The component picks up the video stream with the closest possible (but not exceeding) bit rate to the specified value. If all video streams in the Adaptive Video Set have higher quality than the specified value, the logic chooses the bit rate with the lowest quality. </p> </td> 
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
