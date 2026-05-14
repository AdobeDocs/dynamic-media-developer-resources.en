---
title: External video support
description: The viewer supports playing video hosted outside of Dynamic Media Classic or Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b592f03b-92ab-47d8-96a6-87982fedc901
TQID: 'https://experienceleague.adobe.com/RCjgY-azk-9IIQyK6-Xz4ju6ev3Otbfs1UFvs3j385U'
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
# External video support{#external-video-support}

The viewer supports playing video hosted outside of Dynamic Media Classic or Adobe Experience Manager, Dynamic Media.

 Supported formats for the external video are either MP4 in H.264 format or M3U8 manifest for HLS stream.

The viewer can work either Dynamic Media Classic or Experience Manager Dynamic Media video or with external video. If the viewer starts with Dynamic Media Classic/AEM Dynamic Media video, it should be used with such asset type going forward. It is not possible to load an external video into this viewer using [setVideo](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-setvideo.md#reference-85d3422d6ce64a36ac74827120b5a17c) method and conversely. That is, if the viewer was initially loaded with external video, it continues to work with external videos only.

When working with external video, the viewer ignores the value of any playback modifier and detects the playback type from the external video extension. If the external video URL ends with `.m3u8`, the viewer is using HLS playback; otherwise, progressive playback is used.
