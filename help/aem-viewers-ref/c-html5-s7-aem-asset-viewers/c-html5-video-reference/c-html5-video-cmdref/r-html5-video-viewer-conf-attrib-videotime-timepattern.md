---
description: Configuration attribute for Video Viewer.
seo-description: Configuration attribute for Video Viewer.
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
uuid: 211e0107-b6d1-43d6-b79d-34ed54383f80
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
---

# VideoTime.timepattern{#videotime-timepattern}

Configuration attribute for Video Viewer.

 `[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Sets the pattern for the time that is displayed in the control bar, where <span class="codeph"> h</span> is hours, <span class="codeph"> m</span> is minutes, and <span class="codeph"> s</span> is seconds. </p> <p>The number of letters used for each time unit determines the number of digits to display for the unit. If the number cannot fit into the given digits, the equivalent value is displayed in the subsequent unit. </p> <p>For example, if the current movie time is 67 minutes and 5 seconds, the time pattern <span class="codeph"> m:ss</span> shows as 67:05. The same time is displayed as 1:07:5 if the given time pattern is <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```

