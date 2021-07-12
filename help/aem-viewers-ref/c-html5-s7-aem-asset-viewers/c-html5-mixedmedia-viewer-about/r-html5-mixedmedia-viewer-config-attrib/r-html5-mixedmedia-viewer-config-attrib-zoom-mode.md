---
description: Sets the type of zoom interaction.


solution: Experience Manager
title: zoomMode

feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
---
# zoomMode{#zoommode}

Sets the type of zoom interaction.

 `zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuous </span> enables classic zoom where the image gradually zooms in as you click, double-tap, or pinch out in the main view. You need to explicitly zoom out or reset the zoom state to get back to the initial view. </p> <p> <span class="codeph"> inline </span> enables instant zoom, where the zoomed image instantly appears as you hover the main view on desktop or to touch and hold on a touch device; image automatically reverts to initial state once you move your mouse from the view or release your finger. Note that in <span class="codeph"> inline </span> mode nested image sets are flattened and displayed as individual thumbnails. <span class="codeph"> auto </span> activates inline mode on desktop and continuous mode on touch devices. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-65be9301796240e38f31818229da7acc}

Optional.

## Default {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Example {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
