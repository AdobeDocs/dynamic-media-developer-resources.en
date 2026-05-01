---
description: PageView.singleclick
solution: Experience Manager
title: PageView.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffe77be7-bf12-4e9d-9355-2857d366d14e
TQID: https://experienceleague.adobe.com/OenUjMAi8hIxkDgMtQY2IuK8JkEV03eUmJf5gA1GpQc
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
---
# PageView.singleclick{#pageview-singleclick}

 [!DNL `[PageView.|<containerId>_pageView.]singleclick=none|zoom|reset|zoomReset`]

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

[!DNL `zoomReset`] on desktop computers; [!DNL `none`] on touch devices.

## Example {#section-5f63781afec94e0189e135995f686c20}

[!DNL `singleclick=zoom`]
