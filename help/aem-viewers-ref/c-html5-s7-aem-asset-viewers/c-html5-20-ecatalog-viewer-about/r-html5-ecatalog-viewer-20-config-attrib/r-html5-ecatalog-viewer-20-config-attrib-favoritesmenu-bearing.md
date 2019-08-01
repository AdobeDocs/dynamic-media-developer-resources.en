---
description: Specifies the direction of slide animation for the buttons container.
seo-description: Specifies the direction of slide animation for the buttons container.
seo-title: FavoritesMenu.bearing
solution: Experience Manager
title: FavoritesMenu.bearing
topic: Dynamic media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
index: y
internal: n
snippet: y
---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

Specifies the direction of slide animation for the buttons container.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> When set to <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>, or <span class="codeph"> right</span>, the panel rolls out in specified direction without an additional bounds check, which results in panel clipping by an outside container. </p> <p>When set to <span class="codeph"> fit-vertical</span>, the component first shifts the base panel position to the bottom of the Favorites menu and tries to roll out the panel in one of the following directions from such base location: bottom, right, left. With each attempt the component checks if the panel is clipped by an outside container. If all attempts fail, the component tries to shift the base panel position to the top and repeat roll out attempts from a top, right, and left direction. </p> <p>When set to <span class="codeph"> fit-lateral</span>, the component uses a similar logic. The base is shifted to the right first, trying right, down, and up roll out directions. Then, it shifts the base to the left, trying left, down and up roll out directions. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Default {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left` 
