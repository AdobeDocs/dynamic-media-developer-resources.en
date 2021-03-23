---
description: Configuration attribute for Interactive Video Viewer.


solution: Experience Manager
title: VideoPlayer.playback

feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
---

# VideoPlayer.playback{#videoplayer-playback}

Configuration attribute for Interactive Video Viewer.

 `[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Sets the type of playback used by the viewer. </p> <p>When <span class="codeph"> auto</span> is set, in most desktop browsers and all iOS devices the viewer uses HTML5 streaming video in HLS format, and falls back to progressive HTML5 playback on certain systems like older Internet Explorer and Android. </p> <p>When <span class="codeph"> progressive</span> is set, the viewer relies only on HTML5 playback as natively supported by browsers and plays video progressively on all systems. </p> <p>For more information on the playback selection in <span class="codeph"> auto</span> and <span class="codeph"> progressive</span> native modes, see the HTML5 Viewers SDK User Guide. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`auto`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive` 
