---
title: PageView.singleclick
description: PageView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 96896145-f8d9-4fee-abfe-7f9193776993
---
# PageView.singleclick{#pageview-singleclick}

 `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_5654736F216D4ABC9FC783F83E0BBA03"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configures the mapping of single-click/tap to zoom actions. Setting to <span class="codeph"> none </span> disables single-click/tap zoom. If set to <span class="codeph"> zoom </span> clicking the image zooms in one zoom step; CTRL+Click zooms out one zoom step. Setting to <span class="codeph"> reset </span> causes a single click on the image to reset the zoom to the initial zoom level. For <span class="codeph"> zoomReset </span>, reset is applied if the current zoom factor is at or beyond the specified limit, otherwise zoom is applied. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-edcfcd6c0bd24ac093442c56450b3c97}

Optional.

## Default {#section-58cbfe8a90214c49bbbfb7e83c569d75}

`zoomReset` on desktop computers; `none` on touch devices.

## Example {#section-5f63781afec94e0189e135995f686c20}

`singleclick=zoom`
