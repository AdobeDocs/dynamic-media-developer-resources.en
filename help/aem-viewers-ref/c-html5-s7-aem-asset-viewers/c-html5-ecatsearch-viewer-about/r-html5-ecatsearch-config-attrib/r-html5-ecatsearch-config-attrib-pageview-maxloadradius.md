---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cf769b2d-be4e-4d93-9620-00a438157693
---
# PageView.maxloadradius{#pageview-maxloadradius}

 [!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Specifies the component preload behavior. </p> <p>When set to <span class="codeph"> -1</span> the component preloads all the catalog frames when in an idle state. </p> <p> When set to <span class="codeph"> 0</span> the component loads only the frame that is visible, the previous frame, and the next frame. </p> <p>Set <span class="codeph"><span class="varname"> preloadnbr</span></span> to define how many invisible frames around the currently displayed frame are preloaded in an idle state. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-4b7952997f9240e581d21bcdb173f9af}

Optional.

## Default {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Example {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
