---
title: VideoPlayer.playback
description: Configuration attribute for Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
TQID: 'https://experienceleague.adobe.com/kWCkzBjr6vJAyCk6PareJcg8AfwNvm2gNcEC5BpZXxE'
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
# VideoPlayer.playback{#videoplayer-playback}

Configuration attribute for Video Viewer.

 `[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Sets the type of playback used by the viewer. When <span class="codeph"> auto</span> is set, on most desktop browsers and all iOS devices, the viewer uses HTML5 streaming video in HLS format. It falls back to progressive HTML5 playback on certain systems like older Internet Explorer and Android™. </p> <p>If <span class="codeph"> progressive</span> is specified, the viewer relies only on HTML5 playback as natively supported by browsers and plays video progressively on all systems. </p> <p>For more information on the playback selection in auto and progressive modes, consult the Viewer SDK User Guide. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

Ignored when viewer works with external video. See [External Video Support](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
