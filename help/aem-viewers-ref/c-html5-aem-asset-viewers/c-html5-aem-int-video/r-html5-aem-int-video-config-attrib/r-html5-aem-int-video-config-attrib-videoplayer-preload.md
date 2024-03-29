---
title: VideoPlayer.preload
description: Indicates whether the viewer begins loading video content before the playback starts.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: afabbfde-e003-4fee-a4ef-0fc4c43fd960
---
# VideoPlayer.preload{#videoplayer-preload}

Indicates whether the viewer begins loading video content before the playback starts.

 `[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> If set to <span class="codeph"> 1 </span> the video begins to download right after the asset is set; otherwise, preload starts only after the playback is initiated by the end user or an API call. </p> <p>If set to <span class="codeph"> 0 </span> certain features may not work until playback starts; specifically, the seek operation does not update the video frame. If poster image is disabled, the viewer shows as an empty area instead of the first video frame. </p> <p>Disabling video preload may be ignored on certain versions of Internet Explorer 11 and Edge browsers. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
