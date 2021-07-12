---
description: Configuration attribute for Interactive Video Viewer.
solution: Experience Manager
title: InteractiveSwatches.scrollstep
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 15bf7af8-428b-4c1c-b7ad-004563347d7c
---
# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

Configuration attribute for Interactive Video Viewer.

 ` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`step`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p>Specifies the number of swatches to scroll for each tap of the corresponding scroll button. </p> <p>If the specified value is greater than the number of interactive swatches visible, each tap only scrolls by the number of visible swatches to prevent the omission of any swatch. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Default {#section-71fb773f814649b2885aefee68073641}

`3`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
scrollstep=1
```
