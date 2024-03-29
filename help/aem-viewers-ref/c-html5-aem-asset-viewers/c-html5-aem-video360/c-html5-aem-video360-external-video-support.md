---
title: External video support
description: The viewer supports playing video hosted outside of Dynamic Media Classic or Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
---
# External video support{#external-video-support}

The viewer supports playing video hosted outside of Dynamic Media Classic or Adobe Experience Manager, Dynamic Media.

 Supported formats for the external video are either MP4 in H.264 format or M3U8 manifest for HLS stream.

The viewer can work either Dynamic Media Classic or Experience Manager Dynamic Media video or with external video. If the viewer starts with Dynamic Media Classic/AEM Dynamic Media video, it should be used with such asset type going forward. It is not possible to load an external video into this viewer using [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) method and conversely. That is, if the viewer was initially loaded with external video, it continues to work with external videos only.

When working with external video, the viewer ignores the value of any playback modifier and detects the playback type from the external video extension. If the external video URL ends with `.m3u8`, the viewer is using HLS playback; otherwise, progressive playback is used.
