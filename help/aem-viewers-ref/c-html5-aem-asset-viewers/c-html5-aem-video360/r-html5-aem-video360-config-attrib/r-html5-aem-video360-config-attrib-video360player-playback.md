---
description: Configuration attribute for Video360 Viewer.
seo-description: Configuration attribute for Video360 Viewer.
seo-title: Video360Player.playback
solution: Experience Manager
title: Video360Player.playback
uuid: ce814963-5cb8-408e-9d57-e7b7e61e0fab
feature: "Dynamic Media Classic,Viewers,SDK/API,360 VR Video"
role: "Developer,Business Practitioner"
---

# Video360Player.playback{#video-player-playback}

Configuration attribute for Video360 Viewer.

 `[Video360Player.|<containerId>_video360Player.]playback=auto|progressive`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Sets the type of playback used by the viewer. </p> <p>When <span class="codeph"> auto</span> is set, in most desktop browsers and all iOS devices the viewer uses HTML5 streaming video in HLS format, and falls back to progressive HTML5 playback on certain systems like older Internet Explorer and Android. </p> <p>When <span class="codeph"> progressive</span> is set, the viewer relies only on HTML5 playback as natively supported by browsers and plays video progressively on all systems. </p> <p>For more information on the playback selection in <span class="codeph"> auto</span> and <span class="codeph"> progressive</span> native modes, see the HTML5 Viewers SDK User Guide. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional. Ignored when the viewer works with external video.

See [External video support](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) for details.

## Default {#section-71fb773f814649b2885aefee68073641}

`auto`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

`playback=progressive` 
