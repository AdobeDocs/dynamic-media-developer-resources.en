---
title: External video support
description: The viewer supports playing video hosted outside of Dynamic Media Classic or Adobe Experience Manager - Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b42e67cb-6959-4eea-8d45-49481e0e9d80
---
# External video support{#external-video-support}

The viewer supports playing video hosted outside of Dynamic Media Classic or Adobe Experience Manager - Dynamic Media.

 Supported formats for the external video are either MP4 in H.264 format or M3U8 manifest for HLS stream.

The viewer can work either Dynamic Media Classic or Experience Manager - Dynamic Media video or with external video. If the viewer starts with Dynamic Media Classic/Dynamic Media video, use it with such asset type going forward, it is not possible to load an external video into this viewer using [ `setVideo`](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) method. And vice verse: if viewer was initially loaded with external video, it should keep working with external videos only.

When working with external video, the viewer ignores the value of playback modifier and detects the playback type from the external video extension. If external video URL ends with `.m3u8` the viewer is using HLS playback, otherwise progressive playback is used.
