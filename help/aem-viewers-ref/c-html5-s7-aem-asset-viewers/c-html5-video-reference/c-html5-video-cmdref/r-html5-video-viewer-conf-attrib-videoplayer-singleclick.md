---
title: VideoPlayer.singleclick
description: Configuration attribute for Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
TQID: 'https://experienceleague.adobe.com/RH1L9ADikh3LiDMwfqDdrGOZ7L08nRyFgIly2yCKZf4'
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
# VideoPlayer.singleclick{#videoplayer-singleclick}

Configuration attribute for Video Viewer.

 ` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configures the mapping of single-click/tap to toggle play/pause. Setting to <span class="codeph"> none</span> disables single-click/tap to play/pause. If set to <span class="codeph"> playPause</span>, clicking the video toggles between playing and pausing the video. On some devices, you can use native controls. In such case, <span class="codeph"> singleclick</span> behavior is disabled. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```
