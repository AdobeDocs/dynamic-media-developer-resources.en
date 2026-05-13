---
title: VideoPlayer.mutevolume
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 84deb0d4-ac7e-4ba0-884f-675a0dcc827b
TQID: 'https://experienceleague.adobe.com/B1HkiDle4bh82Mq2qY9q0mDTlnUl4lIZMOoeE4RPWGA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# VideoPlayer.mutevolume{#videoplayer-mutevolume}

Configuration attribute for Interactive Video Viewer.

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
