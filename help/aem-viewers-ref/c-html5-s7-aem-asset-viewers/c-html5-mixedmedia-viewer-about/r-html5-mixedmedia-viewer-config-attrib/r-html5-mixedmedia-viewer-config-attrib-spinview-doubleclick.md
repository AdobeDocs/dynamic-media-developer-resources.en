---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
---
# SpinView.doubleclick{#spinview-doubleclick}

 `[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configures the mapping of double-click/tap to spin actions. Setting to <span class="codeph"> none </span> disables double-click/tap spin. If set to <span class="codeph"> zoom </span>, clicking the image spins in one spin step; CTRL+Click spins out one spin step. Setting to <span class="codeph"> reset </span> causes a single click on the image to reset the spin to the initial spin level. For <span class="codeph"> zoomReset </span>, reset is applied if the current spin factor is at or beyond the specified limit, otherwise spin is applied. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` On desktop computers; `zoomReset` on touch devices.

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
