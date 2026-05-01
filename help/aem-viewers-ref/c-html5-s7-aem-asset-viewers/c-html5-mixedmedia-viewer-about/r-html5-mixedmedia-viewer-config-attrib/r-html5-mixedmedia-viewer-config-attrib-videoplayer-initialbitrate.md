---
title: VideoPlayer.initialbitrate
description: VideoPlayer.initialbitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
TQID: https://experienceleague.adobe.com/WBphRQUYTrIqpHtmTyWv0suq0Sakezqciokicde75-0
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

 ` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
   <td colname="col2"> <p>Sets the video bitrate (in kilobits per seconds or kbps) that is used for initial playback of video on desktops. </p> <p>If this bitrate value does not exist in the Adaptive Video Set, then the video player starts the video that has the next lowest bitrate. </p> <p>If set to <span class="codeph"> 0 </span>, the video player starts from the lowest possible bitrate. Applicable only for systems that do not have native support for HTML5 HLS video (which are Firefox, Chrome and Internet Explorer 11 browsers on Windows 10), and when playback mode is set to <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
