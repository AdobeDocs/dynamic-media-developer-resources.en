---
description: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick

feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 2ec6d871-05d9-4d85-b031-e64386f5d2e9
---
# VideoPlayer.singleclick{#videoplayer-singleclick}

 ` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_53A26E1617CB411B9586203CB9AA1AB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configures the mapping of single-click/tap to toggle play/pause. Setting to <span class="codeph"> none</span> disables single-click/tap to play/pause. If set to <span class="codeph"> playPause</span>, clicking the video toggles between playing and pausing the video. On some devices, you can use native controls. In such case, <span class="codeph"> singleclick</span> behavior is disabled. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`playPause`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=none`
