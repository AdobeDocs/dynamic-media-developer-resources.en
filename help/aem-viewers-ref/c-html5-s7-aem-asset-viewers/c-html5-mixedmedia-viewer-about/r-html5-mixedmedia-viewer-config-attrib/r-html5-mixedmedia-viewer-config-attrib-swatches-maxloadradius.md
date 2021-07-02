---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius

feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,Business Practitioner
exl-id: 06f493d7-18c9-4bb1-add6-a0dfd1a689bd
---
# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_012E1D178BFA4BD9814A7AAD2B4403BB"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Specifies the component preload behavior. When set to <span class="codeph"> -1</span> all swatches are loaded simultaneously when the component is initialized or the asset is changed. </p> <p>When set to <span class="codeph"> 0</span> only visible swatches are loaded. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> defines how many invisible rows/columns around the visible area are preloaded. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=-1`
