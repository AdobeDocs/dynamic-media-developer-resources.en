---
title: VideoPlayer.mutevolume
description: Configuration attribute for Mixed Media Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 13398ac5-7137-4345-88b8-5e4df09edb7b
TQID: https://experienceleague.adobe.com/YYDVyRrpuZfUX9ymQvP-ZrbSRrOFrDVJQNg0natHv3o
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# VideoPlayer.mutevolume{#videoplayer-mutevolume}

Configuration attribute for Mixed Media Video Viewer.

 `[VideoPlayer.|<containerId>_videoPlayer.]mutevolume=0|1`

<table id="table_2A4F898BBF88417DB0834B7F78637F5D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Sets muted mode for video playback on initial load. If set to <span class="codeph"> 1 </span> the volume is muted; otherwise, the video plays with sound. On certain devices, muting video playback on load also allows the video to auto play. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`mutevolume=1`
