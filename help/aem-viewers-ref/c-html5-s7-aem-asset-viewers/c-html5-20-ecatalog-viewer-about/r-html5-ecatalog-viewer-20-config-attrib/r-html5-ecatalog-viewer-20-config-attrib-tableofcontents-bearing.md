---
title: TableOfContents.bearing
description: TableOfContents.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
---
# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> Controls the direction of the drop-down panel appearance. </p> <p>When set to <span class="codeph"> fit-vertical</span>, the component first shifts the base panel position to the bottom of its button and tries to roll out the panel either right or left from the base location. With each attempt, the component checks if the panel is clipped by an outside container. If all attempts fail, the component tries to shift the base panel position to the top and repeat rollout attempts in the right and left direction. </p> <p>When set to <span class="codeph"> fit-lateral</span>, the component uses a similar logic, but shifts the base to the right first, trying down and up rollout directions. Then, it shifts the base to the left, trying down and up rollout directions. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Sets the delay in seconds for the drop-down auto-hide timer which hides the panel when a user is idle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-55436ddd78b04f538dbb9a7a8463feae}

Optional.

## Default {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## Example {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
