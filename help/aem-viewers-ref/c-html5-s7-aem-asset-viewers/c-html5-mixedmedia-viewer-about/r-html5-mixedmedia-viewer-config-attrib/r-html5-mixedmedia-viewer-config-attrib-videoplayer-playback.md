---
description: Configuration attribute for Mixed Media Video Viewer.
seo-description: Configuration attribute for Mixed Media Video Viewer.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
feature: "Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets"
role: "Developer,Business Practitioner"
---

# VideoPlayer.playback{#videoplayer-playback}

Configuration attribute for Mixed Media Video Viewer.

 `[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Sets the type of playback used by the viewer. When <span class="codeph"> auto</span> is set, on most desktop browsers and all iOS devices, the viewer uses HTML5 streaming video in HLS format. It falls back to progressive HTML5 playback on certain systems like older Internet Explorer and Android. </p> <p>If <span class="codeph"> progressive</span> is specified, the viewer relies only on HTML5 playback as natively supported by browsers and plays video progressively on all systems. </p> <p>For more information on the playback selection in auto and progressive modes please consult the Viewer SDK User Guide. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive` 
