---
description: PageView.doubleclick
solution: Experience Manager
title: PageView.doubleclick

feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e6baef83-b4a8-4bef-bb13-263f3875030d
---
# PageView.doubleclick{#pageview-doubleclick}

 [!DNL `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`]

<table id="table_942C8BDBDE1B441596987E9E971202E7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configures the mapping of double-click/tap to zoom actions. Setting to <span class="codeph"> none </span> disables double-click/tap zoom. If set to <span class="codeph"> zoom </span> clicking the image zooms in one zoom step; CTRL+Click zooms out one zoom step. Setting to <span class="codeph"> reset </span> causes a single click on the image to reset the zoom to the initial zoom level. For <span class="codeph"> zoomReset </span>, reset is applied if the current zoom factor is at or beyond the specified limit, otherwise zoom is applied. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-03b915a16cf943afadc1bbaa4ef8e2eb}

Optional.

## Default {#section-814d6bc6a0834005a0a72c7040e45693}

[!DNL `reset`] on desktop computers; [!DNL `zoomReset`] on touch devices.

## Example {#section-986e7672f3694b7aa7572fb4428172ca}

[!DNL `doubleclick=zoom`]
