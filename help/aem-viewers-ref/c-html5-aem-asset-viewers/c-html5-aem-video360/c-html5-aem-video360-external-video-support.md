---
description: The viewer supports playing video hosted outside of SPS or AEM Dynamic Media.
seo-description: The viewer supports playing video hosted outside of SPS or AEM Dynamic Media.
seo-title: External video support
solution: Experience Manager
title: External video support
topic: Dynamic media
uuid: 2e9f1c54-627f-4462-ae85-8a5ca1d09762
index: y
internal: n
snippet: y
---

# External video support{#external-video-support}

The viewer supports playing video hosted outside of SPS or AEM Dynamic Media.

 Supported formats for the external video are either MP4 in H.264 format or M3U8 manifest for HLS stream.

The viewer can work either Dynamic Media Classic or AEM Dynamic Media video or with external video. If the viewer starts with Dynamic Media Classic/AEM Dynamic Media video, it should be used with such asset type going forward. It is not possible to load an external video into this viewer using [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) method and vice versa. That is, if the viewer was initially loaded with external video, it continues to work with external videos only.

When working with external video the viewer ignores the value of any playback modifier and detects the playback type from the external video extension. If the external video URL ends with `.m3u8`, the viewer is using HLS playback; otherwise, progressive playback is used. 
