---
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
---
# SocialShare.bearing{#socialshare-bearing}

Configuration attribute for Interactive Video Viewer.

 `[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Specifies the direction of slide animation for buttons container. When set to <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>, or <span class="codeph"> right</span>, the panel rolls out in the specified direction without any additional bounds checking, which may result in the panel being clipped by an outside container. </p> <p>When set to <span class="codeph"> fit-vertical</span>, the component first shifts the base panel position to the bottom of SocialShare and tries to roll out the panel in one of the following directions from such a base location: bottom, right, left. With each attempt the component checks if panel is clipped by an outside container. If all attempts fail, the component tries to shift the base panel position to the top and repeats the roll out attempts from a top, right, and left direction. </p> <p>When set to <span class="codeph"> fit-lateral</span>, the component uses a similar logic, but shifts the base to the right first, ttrying right, down, and up rollout directions. Then, it shifts the base to the left, trying left, down and up rollout directions. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```
