---
title: PageView.doubleclick
description: PageView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d53a8723-d710-4722-b1a7-c88d3b9d270b
TQID: https://experienceleague.adobe.com/JLystfRWIa0YDmgtKBo0aHwT3yVN2Dyjy0GcW-gshkA
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# PageView.doubleclick{#pageview-doubleclick}

 `[PageView.|<containerId>_pageView.]doubleclick=none|zoom|reset|zoomReset`

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

`reset` on desktop computers; `zoomReset` on touch devices.

## Example {#section-986e7672f3694b7aa7572fb4428172ca}

`doubleclick=zoom`
