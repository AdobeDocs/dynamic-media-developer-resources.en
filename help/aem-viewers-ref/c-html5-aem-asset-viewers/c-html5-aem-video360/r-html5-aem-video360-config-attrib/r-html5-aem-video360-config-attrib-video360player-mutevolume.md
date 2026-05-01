---
title: Video360Player.mutevolume
description: Configuration attribute for Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 8f95c01f-e634-4d6c-a22f-c2285ee969c8
TQID: https://experienceleague.adobe.com/cvKojcHCFGCQWyfgp6T2wEG6Bi1Yst6c2QTwIC1-b3g
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# Video360Player.mutevolume{#video-player-mutevolume}

Configuration attribute for Video360 Viewer.

 `[Video360Player.|<containerId>_video360Player.]mutevolume=0|1`

<table id="table_2A4F898BBF88417DB0834B7F78637F5D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Sets muted mode for video playback on initial load. If set to <span class="codeph"> 1 </span> the volume is muted; otherwise, the video plays with sound. On certain devices, muting video playback on load also lets the video auto play. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`mutevolume=1`
