---
description: Configuration attribute for Video360 Viewer.
seo-description: Configuration attribute for Video360 Viewer.
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
uuid: 43217e2e-71c5-4c58-94e0-c6ed38e25a5b
feature: "Dynamic Media Classic,Viewers,SDK/API,360 VR Video"
role: "Developer,Business Practitioner"
---

# SocialShare.bearing{#socialshare-bearing}

Configuration attribute for Video360 Viewer.

 `[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Specifies the direction of the slide animation for the buttons container. </p> <p> When set to <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>, or <span class="codeph"> right</span>, the panel rolls out in a specified direction without an additional bounds check, which can result in panel clipping by an outside container. </p> <p>When set to <span class="codeph"> fit-vertical</span>, the component first shifts the base panel position to the bottom of SocialShare and tries to roll out the panel from the bottom, right, or left from such base location. With each attempt the component checks if the panel is clipped by an outside container. If all attempts fail, the component tries to shift the base panel position to the top and repeat roll out attempts in the top, right, and left direction. </p> <p>When set to <span class="codeph"> fit-lateral</span>, the component uses a similar logic. However it shifts the base to the right first, trying right, down, and up rollout directions, and then shifts the base to the left, trying left, down, and up rollout directions. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```

