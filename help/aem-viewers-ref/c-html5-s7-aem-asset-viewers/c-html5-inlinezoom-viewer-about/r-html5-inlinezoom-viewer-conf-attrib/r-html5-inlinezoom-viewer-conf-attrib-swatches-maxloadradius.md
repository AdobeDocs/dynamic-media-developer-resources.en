---
title: Swatches.maxloadradius
description: Swatches.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 574cb37c-009a-43c7-ae55-8b26c0c096c5
---
# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the component preload behavior. When set to <span class="codeph"> -1</span> all swatches are loaded simultaneously when component is initialized or asset changed. When set to <span class="codeph"> 0</span> only visible swatches are loaded. </p> <p><span class="codeph"> <span class="varname"> preloadnbr</span></span> defines how many invisible rows/columns around the visible area are preloaded. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-e6310c8c4e8547689a5b48ceddb3671d}

Optional.

## Default {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1`

## Example {#section-3a188ab955c445bcb2efa3c49722c10d}

`maxloadradius=-1`
