---
title: VideoTime.timepattern
description: VideoTime.timepattern
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0c79b3e2-ac5a-43c3-ac52-8240e7ed3cc1
TQID: https://experienceleague.adobe.com/4Qu-Hjdk-crAhmJHPWNNdqwA9zu-si9XbiOFBSnJkXE
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# VideoTime.timepattern{#videotime-timepattern}

 `[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Sets the pattern for the time that is displayed in the control bar, where <span class="codeph"> h</span> is hours, <span class="codeph"> m</span> is minutes, and <span class="codeph"> s</span> is seconds. </p> <p>The number of letters used for each time unit determines the number of digits to display for the unit. If the number cannot fit into the given digits, the equivalent value is displayed in the subsequent unit. </p> <p>For example, if the current movie time is 67 minutes and 5 seconds, the time pattern <span class="codeph"> m:ss</span> shows as 67:05. The same time is displayed as 1:07:5 if the given time pattern is <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
