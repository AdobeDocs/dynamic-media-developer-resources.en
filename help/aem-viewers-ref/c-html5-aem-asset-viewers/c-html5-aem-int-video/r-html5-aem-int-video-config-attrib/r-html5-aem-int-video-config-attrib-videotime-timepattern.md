---
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
title: VideoTime.timepattern
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: de071adf-6c3c-4702-8950-8246b8ee459e
---
# VideoTime.timepattern{#videotime-timepattern}

Configuration attribute for Interactive Video Viewer.

 `[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Sets the pattern for the time that is displayed in the control bar, where <span class="codeph"> h</span> represents hours, <span class="codeph"> m</span> for minutes, and <span class="codeph"> s</span> for seconds. </p> <p>The number of letters used for each time unit determines the number of digits to display for the unit. If the number cannot fit into the given digits, the equivalent value is displayed in the subsequent unit. </p> <p>For example, if the current movie time is 67 minutes and 5 seconds, a time pattern of <span class="codeph"> m:ss</span> displays as 67:05. The same time is displayed as 1:07:5 if the time pattern is <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```
