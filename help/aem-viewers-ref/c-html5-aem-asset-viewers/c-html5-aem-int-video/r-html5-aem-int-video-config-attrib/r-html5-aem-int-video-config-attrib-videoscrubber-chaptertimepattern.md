---
title: VideoScrubber.chaptertimepattern
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 93c1d38c-1f45-4794-8084-f520f9caf257
TQID: 'https://experienceleague.adobe.com/Md2edYK3N0jOA-KSqNXq1ttto1-3-tIgcWOkspphIqA'
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
# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Configuration attribute for Interactive Video Viewer.

 `[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Sets the pattern for the time that is displayed in the title bar of the chapter label, where <span class="codeph"> h</span> represents hours, <span class="codeph"> m</span> for minutes, and <span class="codeph"> s</span> for seconds. </p> <p>The number of letters used for each time unit determines the number of digits to display for the unit. If the number cannot fit into the given digits, the equivalent value is displayed in the subsequent unit. </p> <p>For example, if the current movie time is 67 minutes and 5 seconds, a time pattern of <span class="codeph"> m:ss</span> displays as 67:05. The same time is displayed as 1:07:5 if the time pattern is <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
chaptertimepattern=h:mm:ss
```
