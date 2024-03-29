---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
---
# SocialShare.bearing{#socialshare-bearing}

 `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> Specifies the direction of slide animation for the buttons container. </p> <p> When set to <span class="codeph"> up </span>, <span class="codeph"> down </span>, <span class="codeph"> left </span>, or <span class="codeph"> right </span>, the panel rolls out in a specified direction without an extra bounds check. This behavior can result in panel clipping by an outside container. </p> <p>When set to <span class="codeph"> fit-vertical </span>, the component first shifts the base panel position to the bottom of SocialShare and try to roll out the panel either from the bottom, right, or left, from such base location. With each attempt, the component checks to see if panel is clipped by an outside container. If all attempts fail, the component tries to shift the base panel position to the top and repeat the rollout attempts from the top, right, and left direction. </p> <p>When set to <span class="codeph"> fit-lateral </span>, the component uses a similar logic as with fit-vertical. However, it shifts the base to the right first-trying right, down, and up roll out directions-and then shifts the base to the left, trying left, down, and up rollout directions. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-8e843b967237426e9a8b3cd0f27b9820}

Optional.

## Default {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Example {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
