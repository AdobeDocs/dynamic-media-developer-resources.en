---
description: Configuration attribute for Video Viewer.
seo-description: Configuration attribute for Video Viewer.
seo-title: VideoScrubber.chaptertimepattern
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
uuid: 75338fa6-83ab-4cb8-babf-e958f97c1b6e
feature: "Dynamic Media Classic,Viewers,SDK/API,Video"
role: "Developer,Business Practitioner"
---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Configuration attribute for Video Viewer.

 `[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Sets the pattern for the time that is displayed in the title bar of the video chapter label, where <span class="codeph"> h</span> is hours, <span class="codeph"> m</span> is minutes, and <span class="codeph"> s</span> is seconds. </p> <p>The number of letters used for each time unit determines the number of digits to display for the unit. If the number cannot fit into the given digits, the equivalent value is displayed in the subsequent unit. </p> <p>For example, if the current movie time is 67 minutes and 5 seconds, the time pattern <span class="codeph"> m:ss</span> shows as 67:05. The same time is displayed as 1:07:5 if the given time pattern is <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```

