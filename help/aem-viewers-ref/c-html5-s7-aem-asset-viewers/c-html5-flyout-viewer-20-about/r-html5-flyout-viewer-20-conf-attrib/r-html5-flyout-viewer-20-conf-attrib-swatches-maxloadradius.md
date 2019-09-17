---
description: null
seo-description: null
seo-title: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
topic: Dynamic media
uuid: 3666b947-4a37-4711-90b0-f9c048b588f8
---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Specifies the component preload behavior. When set to <span class="codeph"> -1</span> all swatches will be loaded simultaneously when component is initialized or asset changed. When set to <span class="codeph"> 0</span> only visible swatches are loaded. </p> <p><span class="codeph"> <span class="varname"> preloadnbr</span></span> defines how many invisible rows/columns around the visible area will be preloaded. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

`1`

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`maxloadradius=-1` 
