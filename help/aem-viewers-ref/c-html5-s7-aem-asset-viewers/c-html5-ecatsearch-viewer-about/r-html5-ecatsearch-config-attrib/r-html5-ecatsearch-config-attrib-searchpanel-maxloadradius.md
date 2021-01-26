---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
topic: Dynamic Media
uuid: 37d58c88-3d45-44d9-9f2c-d616d1077906
---

# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

 [!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Specifies the component preload behavior. </p> <p>When set to <span class="codeph"> -1</span> all thumbnails are loaded simultaneously when the component is initialized or the asset changes. </p> <p> When set to <span class="codeph"> 0</span> only visible thumbnails are loaded. </p> <p>Set <span class="codeph"><span class="varname"> preloadnbr</span></span> to define how many invisible rows around the visible area are preloaded. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-4b7952997f9240e581d21bcdb173f9af}

Optional.

## Default {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Example {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`] 
