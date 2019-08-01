---
description: null
seo-description: null
seo-title: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
index: y
internal: n
snippet: y
---

# SpinView.doubleclick{#spinview-doubleclick}

 `[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configures the mapping of double-click/tap to spin actions. Setting to <span class="codeph"> none </span> disables double-click/tap spin. If set to <span class="codeph"> zoom </span> clicking the image spins in one spin step; CTRL+Click spins out one spin step. Setting to <span class="codeph"> reset </span> causes a single click on the image to reset the spin to the initial spin level. For <span class="codeph"> zoomReset </span>, reset is applied if the current spin factor is at or beyond the specified limit, otherwise spin is applied. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Default {#section-7a2128fd488941948aff18421f533ccf}

`reset` on desktop computers; `zoomReset` on touch devices.

## Example {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom` 
