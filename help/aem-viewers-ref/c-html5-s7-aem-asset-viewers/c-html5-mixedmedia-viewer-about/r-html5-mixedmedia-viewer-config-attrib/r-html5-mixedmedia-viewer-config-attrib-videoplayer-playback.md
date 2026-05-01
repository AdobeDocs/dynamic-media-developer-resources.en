---
title: VideoPlayer.playback
description: Configuration attribute for Mixed Media Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
TQID: https://experienceleague.adobe.com/EdZqPY6W21mJBo8bEM5crFjG9tqMStzpozU1C7t-2Kc
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# VideoPlayer.playback{#videoplayer-playback}

Configuration attribute for Mixed Media Video Viewer.

 `[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Sets the type of playback used by the viewer. When <span class="codeph"> auto</span> is set, on most desktop browsers and all iOS devices, the viewer uses HTML5 streaming video in HLS format. It falls back to progressive HTML5 playback on certain systems like older Internet Explorer and Android™. </p> <p>If <span class="codeph"> progressive</span> is specified, the viewer relies only on HTML5 playback as natively supported by browsers and plays video progressively on all systems. </p> <p>For more information on the playback selection in auto and progressive modes, consult the Viewer SDK User Guide. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
