---
description: null
seo-description: null
seo-title: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
topic: Dynamic media
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
index: y
internal: n
snippet: y
---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Controls the main view highlight appearance when the flyout is active. When set to <span class="codeph"> 0</span>, the area currently visible in the flyout window is highlighted using styles provided by either <span class="codeph"> .s7highlight</span> or <span class="codeph"> .s7cursor</span> CSS class names (depending on the value of <span class="codeph"> highlightmode</span> modifier). When set to <span class="codeph"> 1</span> component enters "inverse" mode where the currently viewed area is either fully transparent (in case <span class="codeph"> highlightmode</span> is set to <span class="codeph"> highlight</span>) or styled with <span class="codeph"> .s7cursor</span> CSS class name (in case <span class="codeph"> highlightmode</span> is set to <span class="codeph"> cursor</span>), but surrounding area is filled using styles provided by <span class="codeph"> .s7overlay</span> CSS class name. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Default {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Example {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1` 
