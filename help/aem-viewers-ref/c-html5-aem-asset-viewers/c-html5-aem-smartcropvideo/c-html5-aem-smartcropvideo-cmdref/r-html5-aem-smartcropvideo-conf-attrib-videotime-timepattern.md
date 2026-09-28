---
title: VideoTime.timepattern
description: Configuration attribute for Smart Crop Video Viewer.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: b63818e2-8da0-4965-b7d6-5ecd7ab5cdca
TQID: 'https://experienceleague.adobe.com/Cm3pgVjX5bs7SgZKgniuSxLD4AcEGgO8Iu6MNugZOvA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# VideoTime.timepattern{#videotime-timepattern}

Configuration attribute for Smart Crop Video Viewer.

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
