---
description: Configuration attribute for Video360 Viewer.
seo-description: Configuration attribute for Video360 Viewer.
seo-title: Video360Player.singleclick
solution: Experience Manager
title: Video360Player.singleclick
uuid: 2972405c-5c89-45d0-a542-19c7463901b4
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
---

# Video360Player.singleclick{#video-player-singleclick}

Configuration attribute for Video360 Viewer.

 `[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configures the mapping of single-click/tap to toggle play/pause. Setting to <span class="codeph"> none</span> disables single-click/tap to play/pause. If set to <span class="codeph"> playPause</span> then clicking on the video toggles between playing and pausing the video. On some devices you can use native controls. In this case, a <span class="codeph"> singleclick</span> behavior is disabled. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`playPause`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```

